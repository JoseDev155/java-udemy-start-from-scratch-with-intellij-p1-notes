# 22. Creando objeto String en la literal vs operador new

## **NOTA IMPORTANTE**: Nuevo proyecto

Se creo un nuevo proyecto llamado `ProgramandoConStrings`:

```plaintext
Project name: ProgramandoConStrings
Project location: C:\Users\usuario\IdeaProjects\ProgramandoConStrings
```

Dentro del `src/` del proyecto creamos una clase llamada `ProgramandoConStrings.java`:

```java
public class ProgramandoConStrings {
}
```

Ejecutamos `psvm` para crear el método `main()`:

```java
public class ProgramandoConStrings {
    public static void main(String[] args) {
        
    }
}
```

## Inciaializar `String`'s

Los `String`'s son un tipo de datos especial y Java nos da muchas facilidades a la hora de trabajar con ellos.

Declarando un `String`:

```java
public class ProgramandoConStrings {
    public static void main(String[] args) {
        String Hola="Hola, gracias por la información";
    }
}
```

Otra forma, usando `new String()`:

```java
public class ProgramandoConStrings {
    public static void main(String[] args) {
        String Hola="Hola, gracias por la información";
        String Hola1=new String("Hola, gracias por la información");
    }
}
```

Para comparar ambas formas, hacemos un `sout`:

```java
public class ProgramandoConStrings {
    public static void main(String[] args) {
        String Hola="Hola, gracias por la información";
        String Hola1=new String("Hola, gracias por la información");
        System.out.println(Hola==Hola1);
    }
}
```

Esto nos devuelve `false`.

Hacemos `sout` de ambos `String`'s:

```java
public class ProgramandoConStrings {
    public static void main(String[] args) {
        String Hola="Hola, gracias por la información";
        String Hola1=new String("Hola, gracias por la información");
        System.out.println(Hola);
        System.out.println(Hola1);
        System.out.println(Hola==Hola1);
    }
}
```

Ambos contienen la misma información.

## Operador `==`

El `false` se da porque el operador `==` nada más compara por valor, osea, deben ser exactamente la misma declaración.

Necesitamos otra declaración igual a `Hola`:

```java
public class ProgramandoConStrings {
    public static void main(String[] args) {
        String Hola="Hola, gracias por la información";
        String Hola3="Hola, gracias por la información";
        String Hola1=new String("Hola, gracias por la información");
        System.out.println(Hola);
        System.out.println(Hola1);
        System.out.println(Hola==Hola3);
    }
}
```

Y esto devuelve `true`.

En Java, cuando declaramos un objeto de tipo `String`, con exaatamente la misma información y declarados de la misma forma, evalua por valor.
En este caso, Java le asignó a `Hola3` el valor de `Hola`.

## Método `equals()`

Para comparar `String`'s, usaremos uno de sus métodos, el método `equals()`:

```java
public class ProgramandoConStrings {
    public static void main(String[] args) {
        String Hola="Hola, gracias por la información";
        String Hola3="Hola, gracias por la información";
        String Hola1=new String("Hola, gracias por la información");
        System.out.println(Hola);
        System.out.println(Hola1);
        System.out.println(Hola.equals(Hola3));
    }
}
```

Esto si nos devuelve `true`.

Con el método `equals()`, los analizamos por su contenido y no por su valor (asignación o declaración), osea, analizamos los caracteres que hay
dentro.