> implementation group: 'com.google.code.gson', name: 'gson', version: '2.9.0'

Serialize and Deserialize Interfaces in Java Using Gson

Gson utils objects:

```groovy
// class GsonObjectWrapper

public class GsonObjectWrapper {
    public static final String CONFIG_LIST_JSON = "data.json";

    private <T> Gson getGsonObject(Type typeOfObject) {
        GsonBuilder builder = new GsonBuilder();
        builder.registerTypeAdapter(typeOfObject, new GsonAdapter<T>());
        return builder.create();
    }

    public <T> void writeContainer(T object, Type typeOfObject) {
        try (var writer = new FileWriter(CONFIG_LIST_JSON)) {
            writer.write(getGsonObject(typeOfObject).toJson(object));
        } catch (Exception e) {
            log.error(e.getMessage());
        }
    }

    public <T> T readContainer(Type typeOfObject, Type typeOfContainer) {
        try (var reader = new FileReader(CONFIG_LIST_JSON)) {
            return getGsonObject(typeOfObject).fromJson(reader, typeOfContainer);
        } catch (Exception e) {
            log.error(e.getMessage());
            return null;
        }
    }
}
```

```groovy
//  class GsonAdapter

public class GsonAdapter<T> implements JsonDeserializer<T>, JsonSerializer<T> {

    private static final String CLASS_NAME = "CLASS_NAME";
    private static final String DATA = "DATA";

    @Override
    public T deserialize(JsonElement json, Type typeOfT, JsonDeserializationContext context) throws JsonParseException {
        JsonObject jsonObject = json.getAsJsonObject();
        JsonPrimitive jsonPrimitive = (JsonPrimitive) jsonObject.get(CLASS_NAME);
        String className = jsonPrimitive.getAsString();
        Class<?> classForName;
        try {
            classForName = Class.forName(className);
            return context.deserialize(jsonObject.get(DATA), classForName);
        } catch (ClassNotFoundException e) {
            log.error(e.getMessage());
            throw new JsonParseException(e.getMessage());
        }
    }

    @Override
    public JsonElement serialize(T object, Type typeOfSrc, JsonSerializationContext context) {
        JsonObject jsonObject = new JsonObject();
        jsonObject.addProperty(CLASS_NAME, object.getClass().getName());
        jsonObject.add(DATA, context.serialize(object));
        return jsonObject;
    }
}
```

Use:

```groovy
// class ActionContainer

public class ActionContainer {
    private List<ActionsInterface> data = new ArrayList<>();
}
```
```groovy
// interface ActionsInterface
// class ActionOne implements ActionsInterface
// class ActionTwo implements ActionsInterface

public interface ActionsInterface {}

public class ActionOne implements ActionsInterface {
    private String description = "text";
}

public class ActionTwo implements ActionsInterface {
    private Integer number = 0;
}
```

```groovy
// class ActionProcessor 

public class ActionProcessor {
    private final GsonObjectWrapper gson = new GsonObjectWrapper();
    private ActionContainer container = new ActionContainer();

    public void load() {
        container = gson.readContainer(ActionsInterface.class, ActionContainer.class);
    }

    public void save() {
        gson.writeContainer(container, ActionsInterface.class);
    }
}
```

data.json: 
```groovy
{
    "data": [
            {"CLASS_NAME": "local.uniclog.model.ActionOne", "DATA":{ "description": "text" }},
            {"CLASS_NAME": "local.uniclog.model.ActionTwo", "DATA":{ "number": 0 }}
    ]
}
```