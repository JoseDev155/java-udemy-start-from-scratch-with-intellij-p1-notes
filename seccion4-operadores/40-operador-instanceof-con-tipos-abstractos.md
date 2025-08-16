# 40. Operador Instanceof con tipos abstractos

Usaremos el mismo programa de la clase anterior:

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

Ahora, preguntamos por el tipo de dato `Long` y hacemos `sout`:

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
        b = num instanceof Long;
        System.out.println(b);
    }
}
```

Y ahora, también vamos a poner el `Double`, `Float`, y hacemos `sout` en cada caso:

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
        b = num instanceof Long;
        System.out.println(b);
        b = num instanceof Double;
        System.out.println(b);
        b = num instanceof Float;
        System.out.println(b);
    }
}
```

Nos marcará errores porque son tipos incompatibles.

Para que nos valide `num`, son números a fin de cuentas, para eso le ponemos la clase `Number`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        String texto = "Hola , ¿Que tal?";
        Number num = 6;

        boolean b = texto instanceof String;
        System.out.println(b);
        b = texto instanceof Object;
        System.out.println(b);
        b = num instanceof Integer;
        System.out.println(b);
        b = num instanceof Object;
        System.out.println(b);
        b = num instanceof Long;
        System.out.println(b);
        b = num instanceof Double;
        System.out.println(b);
        b = num instanceof Float;
        System.out.println(b);
    }
}
```

Ahora ya no nos aparecen los errores. En los 3 casos, nos devuelve `false`.
Como `num` es un número, en la clase `Number` o instancia `Number`, verifica si es `Long`, como no es `Long` devuelve `false`.
No es `Double`, por eso devuelve `false`.
No es `Float`, por eso devuelve `false`.

Entonces, si tenemos un número `Double`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        String texto = "Hola , ¿Que tal?";
        Number num = 6;

        boolean b = texto instanceof String;
        System.out.println(b);
        b = texto instanceof Object;
        System.out.println(b);
        b = num instanceof Integer;
        System.out.println(b);
        b = num instanceof Object;
        System.out.println(b);
        b = num instanceof Long;
        System.out.println(b);
        b = num instanceof Double;
        System.out.println(b);
        b = num instanceof Float;
        System.out.println(b);
        Double a = 2.56;
    }
}
```

Y le ponemos:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        String texto = "Hola , ¿Que tal?";
        Number num = 6;

        boolean b = texto instanceof String;
        System.out.println(b);
        b = texto instanceof Object;
        System.out.println(b);
        b = num instanceof Integer;
        System.out.println(b);
        b = num instanceof Object;
        System.out.println(b);
        b = num instanceof Long;
        System.out.println(b);
        b = num instanceof Double;
        System.out.println(b);
        b = num instanceof Float;
        System.out.println(b);
        Double a = 2.56;
        b = num instanceof Double;
        System.out.println(b);
    }
}
```

Nos devuelve `false`. A pesar de ser un número, en lo que nos tenemos que fijar realmente es en que lo estamos definiendo. Nosotros no podemos
utilizar el `instanceof` con valores primitivos.

`Double` es un tipo primitivo, para poner decimales o flotantes usamos `Number`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        String texto = "Hola , ¿Que tal?";
        Number num = 6;

        boolean b = texto instanceof String;
        System.out.println(b);
        b = texto instanceof Object;
        System.out.println(b);
        b = num instanceof Integer;
        System.out.println(b);
        b = num instanceof Object;
        System.out.println(b);
        b = num instanceof Long;
        System.out.println(b);
        b = num instanceof Double;
        System.out.println(b);
        b = num instanceof Float;
        System.out.println(b);
        Number a = 2.56;
        b = num instanceof Double;
        System.out.println(b);
    }
}
```

Esto devuelve `false`.

## Clase `Number`

Para si nuestro número es de alguna forma, lo ponemos en la clase `Number` y a partir de ahí Java empieza a decir que tipo es.

Pero si ponemos esto:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        String texto = "Hola , ¿Que tal?";
        Number num = 6;

        boolean b = texto instanceof String;
        System.out.println(b);
        b = texto instanceof Object;
        System.out.println(b);
        b = num instanceof Integer;
        System.out.println(b);
        b = num instanceof Object;
        System.out.println(b);
        b = num instanceof Long;
        System.out.println(b);
        b = num instanceof Double;
        System.out.println(b);
        b = num instanceof Float;
        System.out.println(b);
        Number a = 2.56f;
        b = num instanceof Double;
        System.out.println(b);
    }
}
```

Y le pedimos que nos diga si es `Double` o lo que sea, nos sigue devolviendo `false` porque probablemente es un `Float`.