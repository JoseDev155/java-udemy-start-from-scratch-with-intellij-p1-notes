# 26. Métodos importantes del Objeto String 2

Usaremos el mismo programa de la clase anterior:

```java
import java.util.Locale;

public class ProgramandoConStrings {
    public static void main(String[] args) {
        String Nombre="Abraham";
        System.out.println(Nombre.toUpperCase(Locale.ROOT));
        System.out.println(Nombre.toLowerCase(Locale.ROOT));
        System.out.println(Nombre.equals("Abraham"));
        System.out.println(Nombre.equalsIgnoreCase("Abraham"));
        System.out.println(Nombre.compareTo("Andres"));
        System.out.println(Nombre.charAt(0));
        System.out.println(Nombre.charAt(Nombre.length()-1));
    }
}
```

## Más acerca sobre el método `compareTo()`

El `compareTo()` tiene también su contraparte que ignora las mayúsculas.

El `compareTo()` utiliza el orden lexicográfico. Retorna negativo si tiene menos caracteres que el `String` original, retorna `0` si son
iguales, retorna positivo si tiene mas caracteres que el `String` original.

## Método `compareToIgnoreCase()`

Hace lo mismo pero ignorando las mayúsculas. Hacemos un `sout`:

```java
import java.util.Locale;

public class ProgramandoConStrings {
    public static void main(String[] args) {
        String Nombre="Abraham";
        System.out.println(Nombre.toUpperCase(Locale.ROOT));
        System.out.println(Nombre.toLowerCase(Locale.ROOT));
        System.out.println(Nombre.equals("Abraham"));
        System.out.println(Nombre.equalsIgnoreCase("Abraham"));
        System.out.println(Nombre.compareTo("Andres"));
        System.out.println(Nombre.charAt(0));
        System.out.println(Nombre.charAt(Nombre.length()-1));
        System.out.println(Nombre.compareToIgnoreCase("andres"));
    }
}
```

## Método `replace()`

Vamos a reemplazar alguna parte del `Nombre` por algo. Hacemos un `sout`, `replace()` y vamos a reemplazar las `A` por puntos `.`:

```java
import java.util.Locale;

public class ProgramandoConStrings {
    public static void main(String[] args) {
        String Nombre="Abraham";
        System.out.println(Nombre.toUpperCase(Locale.ROOT));
        System.out.println(Nombre.toLowerCase(Locale.ROOT));
        System.out.println(Nombre.equals("Abraham"));
        System.out.println(Nombre.equalsIgnoreCase("Abraham"));
        System.out.println(Nombre.compareTo("Andres"));
        System.out.println(Nombre.charAt(0));
        System.out.println(Nombre.charAt(Nombre.length()-1));
        System.out.println(Nombre.compareToIgnoreCase("andres"));
        System.out.println(Nombre.replace("A", "."));
    }
}
```

## Método `lastIndexOf()`

Vamos a buscar índices.

Hacemos un `sout`, `lastIndexOf()` e ingresamos nuestro caracter que será `a`:

```java
import java.util.Locale;

public class ProgramandoConStrings {
    public static void main(String[] args) {
        String Nombre="Abraham";
        System.out.println(Nombre.toUpperCase(Locale.ROOT));
        System.out.println(Nombre.toLowerCase(Locale.ROOT));
        System.out.println(Nombre.equals("Abraham"));
        System.out.println(Nombre.equalsIgnoreCase("Abraham"));
        System.out.println(Nombre.compareTo("Andres"));
        System.out.println(Nombre.charAt(0));
        System.out.println(Nombre.charAt(Nombre.length()-1));
        System.out.println(Nombre.compareToIgnoreCase("andres"));
        System.out.println(Nombre.replace("A", "."));
        System.out.println(Nombre.lastIndexOf('a'));
    }
}
```

Nos dirá el índice o el último índice en el que aparece la `a`, en este caso es el `5`. Es decir, que si ahora pedimos un `charAt(5)` nos va a
devolver una `a`.

`lastIndexOf()` verifica todo el `String`, ve cuántas veces aparece la `a` y nos da el índice dek caracter del valor que ingresamos.

## Método `indexOf()`

Ahora, queremos específicamente el índice de tal caracter.

Para eso, tomamos una parte del `String`. Hacemos `sout`, `indexOf()` de un `String`:

```java
import java.util.Locale;

public class ProgramandoConStrings {
    public static void main(String[] args) {
        String Nombre="Abraham";
        System.out.println(Nombre.toUpperCase(Locale.ROOT));
        System.out.println(Nombre.toLowerCase(Locale.ROOT));
        System.out.println(Nombre.equals("Abraham"));
        System.out.println(Nombre.equalsIgnoreCase("Abraham"));
        System.out.println(Nombre.compareTo("Andres"));
        System.out.println(Nombre.charAt(0));
        System.out.println(Nombre.charAt(Nombre.length()-1));
        System.out.println(Nombre.compareToIgnoreCase("andres"));
        System.out.println(Nombre.replace("A", "."));
        System.out.println(Nombre.lastIndexOf('a'));
        System.out.println(Nombre.indexOf("braham"));
    }
}
```

Esto nos dirá que es el `1`, es decir, si empezamos desde la `b` su índice es `1`.

Si ahora ponemos:

```java
import java.util.Locale;

public class ProgramandoConStrings {
    public static void main(String[] args) {
        String Nombre="Abraham";
        System.out.println(Nombre.toUpperCase(Locale.ROOT));
        System.out.println(Nombre.toLowerCase(Locale.ROOT));
        System.out.println(Nombre.equals("Abraham"));
        System.out.println(Nombre.equalsIgnoreCase("Abraham"));
        System.out.println(Nombre.compareTo("Andres"));
        System.out.println(Nombre.charAt(0));
        System.out.println(Nombre.charAt(Nombre.length()-1));
        System.out.println(Nombre.compareToIgnoreCase("andres"));
        System.out.println(Nombre.replace("A", "."));
        System.out.println(Nombre.lastIndexOf('a'));
        System.out.println(Nombre.indexOf("am"));
    }
}
```

Nos driá que es el `5`.

Si ahora ponemos:

```java
import java.util.Locale;

public class ProgramandoConStrings {
    public static void main(String[] args) {
        String Nombre="Abraham";
        System.out.println(Nombre.toUpperCase(Locale.ROOT));
        System.out.println(Nombre.toLowerCase(Locale.ROOT));
        System.out.println(Nombre.equals("Abraham"));
        System.out.println(Nombre.equalsIgnoreCase("Abraham"));
        System.out.println(Nombre.compareTo("Andres"));
        System.out.println(Nombre.charAt(0));
        System.out.println(Nombre.charAt(Nombre.length()-1));
        System.out.println(Nombre.compareToIgnoreCase("andres"));
        System.out.println(Nombre.replace("A", "."));
        System.out.println(Nombre.lastIndexOf('a'));
        System.out.println(Nombre.indexOf("m"));
    }
}
```

Nos dirá que es el `6`.

## Método `startsWith()`

Verifica si empieza o termina con algo. Hacemos `sout`, `startsWith()`:

```java
import java.util.Locale;

public class ProgramandoConStrings {
    public static void main(String[] args) {
        String Nombre="Abraham";
        System.out.println(Nombre.toUpperCase(Locale.ROOT));
        System.out.println(Nombre.toLowerCase(Locale.ROOT));
        System.out.println(Nombre.equals("Abraham"));
        System.out.println(Nombre.equalsIgnoreCase("Abraham"));
        System.out.println(Nombre.compareTo("Andres"));
        System.out.println(Nombre.charAt(0));
        System.out.println(Nombre.charAt(Nombre.length()-1));
        System.out.println(Nombre.compareToIgnoreCase("andres"));
        System.out.println(Nombre.replace("A", "."));
        System.out.println(Nombre.lastIndexOf('a'));
        System.out.println(Nombre.indexOf("m"));
        System.out.println(Nombre.startsWith("bra"));
    }
}
```

Nos dirá que es `false` porque no empieza con `bra`.

Pero si ponemos `sout`, `startsWith()`:

```java
import java.util.Locale;

public class ProgramandoConStrings {
    public static void main(String[] args) {
        String Nombre="Abraham";
        System.out.println(Nombre.toUpperCase(Locale.ROOT));
        System.out.println(Nombre.toLowerCase(Locale.ROOT));
        System.out.println(Nombre.equals("Abraham"));
        System.out.println(Nombre.equalsIgnoreCase("Abraham"));
        System.out.println(Nombre.compareTo("Andres"));
        System.out.println(Nombre.charAt(0));
        System.out.println(Nombre.charAt(Nombre.length()-1));
        System.out.println(Nombre.compareToIgnoreCase("andres"));
        System.out.println(Nombre.replace("A", "."));
        System.out.println(Nombre.lastIndexOf('a'));
        System.out.println(Nombre.indexOf("m"));
        System.out.println(Nombre.startsWith("bra"));
        System.out.println(Nombre.startsWith("Abr"));
    }
}
```

Nos dirá que es `true`, porque empieza con eso.

## Método `endsWith()`

La contraparte de `startsWith()`.

Ponemos `sout`, `endsWith()`:

```java
import java.util.Locale;

public class ProgramandoConStrings {
    public static void main(String[] args) {
        String Nombre="Abraham";
        System.out.println(Nombre.toUpperCase(Locale.ROOT));
        System.out.println(Nombre.toLowerCase(Locale.ROOT));
        System.out.println(Nombre.equals("Abraham"));
        System.out.println(Nombre.equalsIgnoreCase("Abraham"));
        System.out.println(Nombre.compareTo("Andres"));
        System.out.println(Nombre.charAt(0));
        System.out.println(Nombre.charAt(Nombre.length()-1));
        System.out.println(Nombre.compareToIgnoreCase("andres"));
        System.out.println(Nombre.replace("A", "."));
        System.out.println(Nombre.lastIndexOf('a'));
        System.out.println(Nombre.indexOf("m"));
        System.out.println(Nombre.startsWith("bra"));
        System.out.println(Nombre.startsWith("Abr"));
        System.out.println(Nombre.endsWith("braham"));
    }
}
```

Nos dirá `true`.

## Método `contains()`

Vamos a verificar si nuestro `String` contiene algo en específico.

Ponemos `sout`, `constians()`, nos pide una secuencia de caracteres este método:

```java
import java.util.Locale;

public class ProgramandoConStrings {
    public static void main(String[] args) {
        String Nombre="Abraham";
        System.out.println(Nombre.toUpperCase(Locale.ROOT));
        System.out.println(Nombre.toLowerCase(Locale.ROOT));
        System.out.println(Nombre.equals("Abraham"));
        System.out.println(Nombre.equalsIgnoreCase("Abraham"));
        System.out.println(Nombre.compareTo("Andres"));
        System.out.println(Nombre.charAt(0));
        System.out.println(Nombre.charAt(Nombre.length()-1));
        System.out.println(Nombre.compareToIgnoreCase("andres"));
        System.out.println(Nombre.replace("A", "."));
        System.out.println(Nombre.lastIndexOf('a'));
        System.out.println(Nombre.indexOf("m"));
        System.out.println(Nombre.startsWith("bra"));
        System.out.println(Nombre.startsWith("Abr"));
        System.out.println(Nombre.endsWith("braham"));
        System.out.println(Nombre.contains("rah"));
    }
}
```

Nos dice `true`.

Si ponemos:

```java
import java.util.Locale;

public class ProgramandoConStrings {
    public static void main(String[] args) {
        String Nombre="Abraham";
        System.out.println(Nombre.toUpperCase(Locale.ROOT));
        System.out.println(Nombre.toLowerCase(Locale.ROOT));
        System.out.println(Nombre.equals("Abraham"));
        System.out.println(Nombre.equalsIgnoreCase("Abraham"));
        System.out.println(Nombre.compareTo("Andres"));
        System.out.println(Nombre.charAt(0));
        System.out.println(Nombre.charAt(Nombre.length()-1));
        System.out.println(Nombre.compareToIgnoreCase("andres"));
        System.out.println(Nombre.replace("A", "."));
        System.out.println(Nombre.lastIndexOf('a'));
        System.out.println(Nombre.indexOf("m"));
        System.out.println(Nombre.startsWith("bra"));
        System.out.println(Nombre.startsWith("Abr"));
        System.out.println(Nombre.endsWith("braham"));
        System.out.println(Nombre.contains("x"));
    }
}
```

Nos dice `false`. Verifica el `String` y ve si contiene el `String` o la cadena de caracteres que hemos ingresado.

## Método `trim()`

Vamos a quitar cosas. Hacemos `sout`, `trim()`:

```java
import java.util.Locale;

public class ProgramandoConStrings {
    public static void main(String[] args) {
        String Nombre="Abraham";
        System.out.println(Nombre.toUpperCase(Locale.ROOT));
        System.out.println(Nombre.toLowerCase(Locale.ROOT));
        System.out.println(Nombre.equals("Abraham"));
        System.out.println(Nombre.equalsIgnoreCase("Abraham"));
        System.out.println(Nombre.compareTo("Andres"));
        System.out.println(Nombre.charAt(0));
        System.out.println(Nombre.charAt(Nombre.length()-1));
        System.out.println(Nombre.compareToIgnoreCase("andres"));
        System.out.println(Nombre.replace("A", "."));
        System.out.println(Nombre.lastIndexOf('a'));
        System.out.println(Nombre.indexOf("m"));
        System.out.println(Nombre.startsWith("bra"));
        System.out.println(Nombre.startsWith("Abr"));
        System.out.println(Nombre.endsWith("braham"));
        System.out.println(Nombre.contains("rah"));
        System.out.println(Nombre.trim());
    }
}
```

En este caso, veremos el `String` tal cual, `Abraham`.

Pero si tuvieramos `Abraham` con mas espacios:

```java
import java.util.Locale;

public class ProgramandoConStrings {
    public static void main(String[] args) {
        String Nombre="  Abraham";
        System.out.println(Nombre.toUpperCase(Locale.ROOT));
        System.out.println(Nombre.toLowerCase(Locale.ROOT));
        System.out.println(Nombre.equals("Abraham"));
        System.out.println(Nombre.equalsIgnoreCase("Abraham"));
        System.out.println(Nombre.compareTo("Andres"));
        System.out.println(Nombre.charAt(0));
        System.out.println(Nombre.charAt(Nombre.length()-1));
        System.out.println(Nombre.compareToIgnoreCase("andres"));
        System.out.println(Nombre.replace("A", "."));
        System.out.println(Nombre.lastIndexOf('a'));
        System.out.println(Nombre.indexOf("m"));
        System.out.println(Nombre.startsWith("bra"));
        System.out.println(Nombre.startsWith("Abr"));
        System.out.println(Nombre.endsWith("braham"));
        System.out.println(Nombre.contains("rah"));
        System.out.println(Nombre.trim());
    }
}
```

Le quita los espacios.