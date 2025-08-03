# 19. Conversiones de tipo primitivos a cadenas

Código de ejemplo:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        boolean cierto=true;
        int entero=5687;
        float flotante=2.56e2f;
        double decimal=23.678;
    }
}
```

## Convirtiendo `boolean` a `String`

Hacemos uso de la clase `Boolean` y usamos el método `toString()`, que lo va a convertir a `String`:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        boolean cierto=true;
        String ciertoConvertido=Boolean.toString(cierto);
        int entero=5687;
        float flotante=2.56e2f;
        double decimal=23.678;
    }
}
```

## Convirtiendo `entero` a `String`

Hacemos:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        boolean cierto=true;
        String ciertoConvertido=Boolean.toString(cierto);
        int entero=5687;
        String enteroConvertido=Integer.toString(entero);
        float flotante=2.56e2f;
        double decimal=23.678;
    }
}
```

## Convirtiendo `float` a `String`

Hacemos:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        boolean cierto=true;
        String ciertoConvertido=Boolean.toString(cierto);
        int entero=5687;
        String enteroConvertido=Integer.toString(entero);
        float flotante=2.56e2f;
        String flotanteConvertido=Float.toString(flotante);
        double decimal=23.678;
    }
}
```

## Convirtiendo `double` a `String`

Hacemos:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        boolean cierto=true;
        String ciertoConvertido=Boolean.toString(cierto);
        int entero=5687;
        String enteroConvertido=Integer.toString(entero);
        float flotante=2.56e2f;
        String flotanteConvertido=Float.toString(flotante);
        double decimal=23.678;
        String decimalConvertido=Double.toString(decimal);
    }
}
```

## Comprobación

Para comprobar el resultado, creamos un `String` y los sumamos o concatenamos todos. También haremos un `sout`:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        boolean cierto=true;
        String ciertoConvertido=Boolean.toString(cierto);
        int entero=5687;
        String enteroConvertido=Integer.toString(entero);
        float flotante=2.56e2f;
        String flotanteConvertido=Float.toString(flotante);
        double decimal=23.678;
        String decimalConvertido=Double.toString(decimal);
        String mensaje=ciertoConvertido+"\n"+enteroConvertido+"\n"+flotanteConvertido+"\n"+decimalConvertido;
        System.out.println(mensaje);
    }
}
```