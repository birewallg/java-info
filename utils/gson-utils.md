> implementation group: 'com.google.code.gson', name: 'gson', version: '2.9.0'


Gson utils

```groovy
// read object
// com.google.gson.Gson

public <T> T read(Type type) {
    try (var reader = new FileReader(filePath)) {
        var token = TypeToken.getParameterized(List.class, type).getType();
        return new Gson().fromJson(reader, token);
    } catch (IOException e) {
        log.error(e.getMessage());
        return null;
    }
}
```
```groovy
// write object
// com.google.gson.Gson

public <T> void write(T object) {
    try (var writer = new FileWriter(filePath)) {
        writer.write(new Gson().toJson(object));
    } catch (IOException e) {
        log.error(e.getMessage());
    }
}
```