## Java Preference

### Get Preference
```java
/**  
 * Preference считывается из реестра, специфичного для конкретной операционной системы.  
 */
public class Demo {
    public static void main(String[] args) {
        Preferences prefs = Preferences.userNodeForPackage(Demo.class);
        String optionValue = prefs.get("option", null);
        // Если preference не был найден, то возвращается null. 
    }
}
```
### Set Preference 
```java
/**
 * Preference сохраняется в реестре, специфичном для конкретной операционной системы.
 */
public class Demo {
    public static void main(String[] args) { 
        Preferences preferences = Preferences.userNodeForPackage(Demo.class); 
        preferences.put("option", "optionValue"); // установить значение
        preferences.remove("option"); // удалить значение
    }
} 
```