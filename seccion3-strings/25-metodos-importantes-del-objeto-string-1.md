# 25. Metodos importantes del Objeto String 1

Código de ejemplo:

```java
public class ProgramandoConStrings {
    public static void main(String[] args) {
        String Nombre="Abraham";
    }
}
```

## Métodos `toUpperCase()` y `toLowerCase()`

Hacemos `sout`:

```java
import java.util.Locale;

public class ProgramandoConStrings {
    public static void main(String[] args) {
        String Nombre="Abraham";
        System.out.println(Nombre.toUpperCase(Locale.ROOT));
        System.out.println(Nombre.toLowerCase(Locale.ROOT));
    }
}
```

El método `toUpperCase()` convierte todo a mayúsculas y el método `toLowerCase()` convierte todo a minúsculas.

## Comparar `String`'s por sus caracteres

Hacemos `sout`:

```java
import java.util.Locale;

public class ProgramandoConStrings {
    public static void main(String[] args) {
        String Nombre="Abraham";
        System.out.println(Nombre.toUpperCase(Locale.ROOT));
        System.out.println(Nombre.toLowerCase(Locale.ROOT));
        System.out.println(Nombre.equals("abraham"));
        System.out.println(Nombre.equalsIgnoreCase("Abraham"));
    }
}
```

El método `equals()` nos devuelve `false`, mientras que el método `equalsIgnoreCase()` nos devuelve `true`.

Esto es porque `Nombre.equals()` nos pide que todos los caracteres, mayúsculas o minúsculas, tengan que ser exactamente los mismos. Y
`Nombre.equalsIgnoreCase()` ignora las mayúsculas y minúsculas.

Ahora, si ponemos el `Nombre.equals()` con la mayúscula:

```java
import java.util.Locale;

public class ProgramandoConStrings {
    public static void main(String[] args) {
        String Nombre="Abraham";
        System.out.println(Nombre.toUpperCase(Locale.ROOT));
        System.out.println(Nombre.toLowerCase(Locale.ROOT));
        System.out.println(Nombre.equals("Abraham"));
        System.out.println(Nombre.equalsIgnoreCase("Abraham"));
    }
}
```

Nos devuelve `true`.

## Método `compareTo()`

Hacemos `sout`:

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
    }
}
```

Esto nos devolverá `-12`, esto es porque está comparando caracter a caracter, ya que hay algunas distancias entre caracteres. Eso es lo que
mide el `compareTo()`.

## Método `charAt()`

Si nada más queremos un caracter de nuestro `String`, si queremos empezar desde el primer caracter o pedir el primer caracter, lo único que
tenemos que hacer es poner `0`, y el último caracter sería el numero natural menos `1`.

Para poner el último y nuestro `String` es muy largo, la instancia `length()` nos devuelve el número de caracteres:

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
        System.out.println(Nombre.charAt(Nombre.length()));
    }
}
```

Esto nos devolverá `A` y un error, ya que el `length()` nos está dando un número que no existe para la consideración del `charAt()`, nos está
dando el número natural.

Le tenemos que restar `1`:

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

Y esto nos devuelve la `m`.