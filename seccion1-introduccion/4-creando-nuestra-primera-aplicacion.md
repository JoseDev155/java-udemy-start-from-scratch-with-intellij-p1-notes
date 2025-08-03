# 4. Creando nuestra primera aplicación

En la pantalla de inicio de IntelliJ, creamos un nuevo proyecto con **New Project**.

## **New Project**

### Personalización

De todas las opciones de personalización:

* Java
* Maven
* Gradle
* Java FX
* Android
* IntelliJ Platform Plugin
* Groovy
* Kotlin

Seleccionamos **Java**.

En **Project SDK**, veremos la versión de Java que descargamos y es la que va a usar el programa.

Si queremos instalar librerías adicionales **Additional Libraries and Frameworks**, podemos seleccionarlas:

* Groovy
* Kotlin/JVM

En nuestro caso, no queremos, no seleccionamos nada. Le damos **Next**.

### **Create project from template**

Nos dirá si queremos crear el proyecto desde alguna plantilla. Como no queremos, no marcamos esa opción.

Le damos **Next**.

### Nombre del proyecto

Le ponemos **HolaMundo**.

La ruta por defecto donde se creará el proyecto es: `C:\Users\usuario\IdeaProjects\HolaMundo`.

Resumen:

```plaintext
Project name: HolaMundo
Project location: C:\Users\usuario\IdeaProjects\HolaMundo
```

**NOTA**: No se recomienda usar espacios en los nombres de los proyectos.

Le damos **Finish**.

## Visualización del Proyecto

Se nos abrirá el proyecto creado. Si expandimos el proyecto, veremos lo siguiente:

* `HolaMundo.iml`: Archivo de configuración del IntelliJ IDEA.
* `.idea/`: Carpeta generada por IntelliJ IDEA.
* `src/`: Carpeta que contendrá los archivos Java de nuestro programa.

Para nuestra primera aplicación, haremos **clic derecho** en `src/`, **New** > **Java Class**, y le pondremos `HolaMundo` (el IDE coloca la extensión `.java` automáticamente).

Y nos abrirá el archivo/clase `HolaMundo.java`:

```java
public class HolaMundo {
}
```