>gradle version 7.1
https://docs.gradle.org/current/userguide/java_library_distribution_plugin.html

Сборка проекта


```groovy
//gradle.build

plugins {
    id 'java'
    id 'java-library-distribution'
}

tasks.jar {
    // optional
    // exclude 'META-INF/*.SF', 'META-INF/*.DSA', 'META-INF/*.RSA', 'META-INF/*.MF'
    
    manifest {
        attributes 'Main-Class': 'local.App',
                'Class-Path': configurations.compileClasspath.files.collect { "lib/$it.name" }.join(' ')
    }
}
```
