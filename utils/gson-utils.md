> implementation group: 'com.google.code.gson', name: 'gson', version: '2.9.0'


Gson utils

```groovy
// read object
// com.google.gson.Gson

    var token = TypeToken.getParameterized(rawType, type).getType();
    OR
    var token = CustomObject.class; 

    var reader = new FileReader(filePath);
    return new Gson().fromJson(reader, token); 
```
```groovy
// write object
// com.google.gson.Gson 

    var writer = new FileWriter(filePath);
    writer.write(new Gson().toJson(object));
```