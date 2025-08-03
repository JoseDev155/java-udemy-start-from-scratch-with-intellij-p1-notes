# 5. Ejemplo Hola Mundo en Java

## Método `main()`

Primero llamaremos al método `main()` (principal), es el método principal del programa. Para hacerlo, haremos uso de un **shortcut** del IDE: `psvm`, y le damos **Enter**.

El resultado será el siguiente:

```java
public class HolaMundo {
    public static void main(String[] args) {
        
    }
}
```

Ahora imprimiremos por consola:

```java
public class HolaMundo {
    public static void main(String[] args) {
        System.out.println("Hola Mundo");
    }
}
```

Un **shortcut** que podemos utilizar para escribir `System.out.println()` es: `sout`, y le damos **Enter**.

Para ejecutarlo, le damos al triángulo **verde** al lado de la clase `HolaMundo` que dice: `Run 'HolaMundo.main()'`. Veremos la salida del programa en la consola del IDE.