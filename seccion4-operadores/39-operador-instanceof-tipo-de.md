# 39. Operador Instanceof (Tipo de)

## ¿Qué es `Instanceof`?

El `Instanceof` es una palabra clave que significa literalmente "instancia de", sin espacio.

Básicamente, su función va a ser determinar si el objeto al que apunta una referencia dada, es una instancia de una clase o interfaz concretas.
Entonces, `Instanceof` devuelve un valor booleano.

El `Instanceof` va a constar de 3 partes:

* Una referencia
* La palabra clave `Instanceof`
* El nombre de la clase o interfaz de la que queremos comprobar si el objeto al que apunta la referencia utilizada es o no una instancia

## Utilizando `Instanceof` en Java

Lo primero que vamos a hacer, es poner un `String`, un `Integer`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        String texto = "Hola , ¿Que tal?";
        Integer num = 6;
    }
}
```

También, vamos a poner un booleano pero usando `Instanceof`.

Vamos a poner el objeto al que queremos preguntar si es una "instancia de":

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        String texto = "Hola , ¿Que tal?";
        Integer num = 6;

        boolean b = texto instanceof String;
    }
}
```

Ponemos un `sout` y sacamos a `b`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        String texto = "Hola , ¿Que tal?";
        Integer num = 6;

        boolean b = texto instanceof String;
        System.out.println(b);
    }
}
```

`texto` es parte de la instancia `String`, nos devuelve `true`. Es para verificar que `texto` que texto es de tipo `String`, de la clase
`String`, es un objeto.

Vamos a ver si `texto` es un objeto (`Object`), y hacemos `sout` de `b`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        String texto = "Hola , ¿Que tal?";
        Integer num = 6;

        boolean b = texto instanceof String;
        System.out.println(b);
        b = texto instanceof Object;
        System.out.println(b);
    }
}
```

Le estamos preguntado a Java si `texto` es un objeto, nos devuelve `true`. Java lo cataloga como objeto o una instancia de tipo objeto.

`texto` no nada mas es una cadena de caracteres, sino una instancia dentro de una clase, está dentro de una clase o activa una clase. En este
caso, es una objeto (`Object`).

Ahora, veremos que `num` sea una instancia de un entero, es decir, le vamos a preguntar a Java si lo considera como entero:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        String texto = "Hola , ¿Que tal?";
        Integer num = 6;

        boolean b = texto instanceof String;
        System.out.println(b);
        b = texto instanceof Object;
        System.out.println(b);
        b = num instanceof Integer;
        System.out.println(b);
    }
}
```

Nos devuelve `true`.

Ahora, vamos a preguntarle, que si es un `Integer`, lo va a considerar como un objeto también.

Y hacemos `sout` de `b`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        String texto = "Hola , ¿Que tal?";
        Integer num = 6;

        boolean b = texto instanceof String;
        System.out.println(b);
        b = texto instanceof Object;
        System.out.println(b);
        b = num instanceof Integer;
        System.out.println(b);
        b = num instanceof Object;
        System.out.println(b);
    }
}
```

Nos devuelve `true`.

Si lo cambiamos por `int`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        String texto = "Hola , ¿Que tal?";
        int num = 6;

        boolean b = texto instanceof String;
        System.out.println(b);
        b = texto instanceof Object;
        System.out.println(b);
        b = num instanceof Integer;
        System.out.println(b);
        b = num instanceof Object;
        System.out.println(b);
    }
}
```

Nos dará error, porque a la hora que trabajamos con `instanceof`, tiene que ser a fuerzas el `Integer`.

`int` no es lo mismo que el `java.lang.Integer`, es decir, cuando ponemos `Integer` es porque `num` es parte de uhna instancia de una
clase.

No es lo mismo agarrar un objeto que el número primitivo. Es decir, el `instanceof` **no puede agarrar datos primitivos**. Pero puede evaluar
`String`'s e `Integer`'s, porque `Integer` le da propiedades de clase o de objeto al número.