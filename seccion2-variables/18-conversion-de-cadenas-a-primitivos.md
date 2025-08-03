# 18. Conversión de cadenas a primitivos

Código de ejemplo:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        String booleano="true";
        String decimales="2.56";
        String entero="395";
        String flotante="2.56e2f";
    }
}
```

Nos conviene saber convertir `String`'s a tipos de datos primitivos, ya que muchas veces que recibamos datos estarán en tipo texto o en una hoja de cálculo, y tendremos que convertirlos
a un tipo de dato en específico.

## Convirtiendo `String` a `boolean`

Hacemos un `sout` y usamos `Boolean.parseBoolean()` para convertirlo en booleano. Si metemos eso mismo en una variable tipo `boolean`, no nos dará error, ya que es de tipo `boolean`:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        String booleano="true";
        boolean booleanoConvertido=Boolean.parseBoolean(booleano);
        System.out.println(Boolean.parseBoolean(booleano));
        String decimales="2.56";
        String entero="395";
        String flotante="2.56e2f";
    }
}
```

## Convirtiendo `String` a `double`

Hacemos:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        String booleano="true";
        boolean booleanoConvertido=Boolean.parseBoolean(booleano);
        System.out.println(Boolean.parseBoolean(booleano));
        String decimales="2.56";
        double decimalesConvertidos=Double.parseDouble(decimales);
        System.out.println(decimalesConvertidos);
        String entero="395";
        String flotante="2.56e2f";
    }
}
```

## Convirtiendo `String` a `entero`

Hacemos:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        String booleano="true";
        boolean booleanoConvertido=Boolean.parseBoolean(booleano);
        System.out.println(Boolean.parseBoolean(booleano));
        String decimales="2.56";
        double decimalesConvertidos=Double.parseDouble(decimales);
        System.out.println(decimalesConvertidos);
        String entero="395";
        int enteroConvertido=Integer.parseInt(entero);
        System.out.println(enteroConvertido);
        String flotante="2.56e2f";
    }
}
```

## Convirtiendo `String` a `float`

Usamos la clase para convertirlo a primitivo. Y hacemos `sout` de `booleano convertido` para no hacer `Boolean.parseBoolean()` dos veces:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        String booleano="true";
        boolean booleanoConvertido=Boolean.parseBoolean(booleano);
        System.out.println(booleanoConvertido);
        String decimales="2.56";
        double decimalesConvertidos=Double.parseDouble(decimales);
        System.out.println(decimalesConvertidos);
        String entero="395";
        int enteroConvertido=Integer.parseInt(entero);
        System.out.println(enteroConvertido);
        String flotante="2.56e2f";
        float flotanteConvertido=Float.parseFloat(flotante);
        System.out.println(flotanteConvertido);
    }
}
```