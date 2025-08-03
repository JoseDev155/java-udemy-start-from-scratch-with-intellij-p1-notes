# 12. Primitivo char o caracter

Las tres formas distintas en que Java acepta caracteres son: UNICODE, ASCII (el estándar) y el caracter simplemente.

Las variables tipo caracter, almacenan un solo caracter en cada una de las variables declaradas.

Para saber cual es el código UNICODE del caracter que queremos.

## CHAR

Las variables tipo caracter se declaran entre comillas simples `''`:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        // UNICODE

        // ASCII

        // CAR
        char simbolo='&';
        System.out.println(simbolo);
    }
}
```

Esto nos imprimirá el caracter `&`. Ahora, ¿cómo escribimos el UNICODE y el ASCII?

## ASCII

Código estándar para el intercambio de información.

Declarando variable con código ASCII:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        // UNICODE

        // ASCII
        char simbolo2=38;
        System.out.println(simbolo2);
        // CAR
        char simbolo='&';
        System.out.println(simbolo);
    }
}
```

Esto nos imprimirá el caracter `&`. Java interpreta el número `38` commo un código ASCII.

## UNICODE

Es otro estándar para el intercambio de información.

* `&` en UNICODE: `U+0026`

Declarando variable con código UNICODE:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        // UNICODE
        char simbolo3='\u0026';
        System.out.println(simbolo3);
        // ASCII
        char simbolo2=38;
        System.out.println(simbolo2);
        // CAR
        char simbolo='&';
        System.out.println(simbolo);
    }
}
```

Esto nos imprimirá el caracter `&`. Si hiciéramos una validación de que Java contempla los 3 como lo mismo, nos diría `true`.

ASCII y UNICODE están basados en otros sistemas numéricos.