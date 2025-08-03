# 7. Ejemplos de variables

## Nuevo proyecto

Creamos un nuevo proyecto llamado `EjemplosVariables`:

```plaintext
Project name: EjemplosVariables
Project location: C:\Users\usuario\IdeaProjects\EjemplosVariables
```

Creamos una nueva clase llamada `EjemplosVariables`:

```java
public class EjemplosVariables {
}
```

Ejecutamos `psvm` para crear el método `main()`:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        
    }
}
```

## Declarar variables

Java no es capaz de interpretar la variable sólo con el nombre. Entonces, lo que hacemos es decir qué tipo de variable es, el nombre que tendrá y darle un valor o dejarla así.

Ejemplos de declaración de variables:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        int edad=20;
        long a=400000000;
        double b=4.56, c=4.5;
        String nombre="Abraham";
        // int[] arreglo= new int[];
    }
}
```

**NOTA**: Siempre cerramos con punto y coma `;`.

También podemos declarar dos variables del mismo tipo en una sola línea.

Usamos `sout` para imprimr una línea. Vamos a imprimir las variables `edad` y `nombre`:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        int edad=20;
        long a=400000000;
        double b=4.56, c=4.5;
        String nombre="Abraham";
        // int[] arreglo= new int[];

        System.out.println(edad);
        System.out.println("Mi nombre es: "+nombre);
    }
}
```

En el caso de `nombre`, usamos el símbolo mas `+` para concatenar.