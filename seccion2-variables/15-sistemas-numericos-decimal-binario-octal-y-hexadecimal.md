# 15. Sistemas numéricos: decimal, binario, octal y hexadecimal

Veremos como manejar algunos de los distintos sistemas numéricos disponibles en Java.

Para esto, necesitamos un entero y lo imprimimos en la consola:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        int numero=450;
        System.out.println("Nuestro numero es: "+numero);
    }
}
```

## Convirtiendo a binario

Vamos a hacer otro `int`:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        int numero=450;
        System.out.println("Nuestro numero es: "+numero);
        int numeroBinario=Integer.toBinaryString(numero);
    }
}
```

Esto nos dará un error, porque esto retorna un `string`, no un `int`.

Entonces, lo declaramos como `string` y vamos a ver cómo se ve ese número binario:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        int numero=450;
        System.out.println("Nuestro numero es: "+numero);
        String numeroBinario=Integer.toBinaryString(numero);
        System.out.println("Numero en binario: "+numeroBinario);
    }
}
```

Esto nos devuelve: `111000010`.

Ahora, para escribir un binario directamente:

* Tomamos el número binario
* Lo escribimos
* Antes de iniciar, le ponemos un `0b`

Ejemplo:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        int numero=450;
        System.out.println("Nuestro numero es: "+numero);
        String numeroBinario=Integer.toBinaryString(numero);
        System.out.println("Numero en binario: "+numeroBinario);
        System.out.println("Numero en binario escrito en Java: "+0b111000010);
    }
}
```

El `0b` le indica a Java que debe leer el número como binario.

El programa nos devuelve `450`. El `0b` hace la conversión a decimal.

## Convirtiendo a hexadecimal

Hacemos:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        int numero=450;
        System.out.println("Nuestro numero es: "+numero);
        String numeroBinario=Integer.toBinaryString(numero);
        System.out.println("Numero en binario: "+numeroBinario);
        System.out.println("Numero en binario escrito en Java: "+0b111000010);
        System.out.println("Numero en hexadecimal: "+Integer.toHexString(numero));
    }
}
```

Esto nos devuelve `1c2`, que es el código para ponerlo en hexadecimal.

Para decir que queremos la numeración hexadecimal en Java:

* Tomamos el código hexadecimal del número
* Lo escribimos
* Antes de iniciar, le ponemos un `0x`

Ejemplo:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        int numero=450;
        System.out.println("Nuestro numero es: "+numero);
        String numeroBinario=Integer.toBinaryString(numero);
        System.out.println("Numero en binario: "+numeroBinario);
        System.out.println("Numero en binario escrito en Java: "+0b111000010);
        System.out.println("Numero en hexadecimal: "+Integer.toHexString(numero));
        System.out.println("Numero en hexadecimal escrito en Java: "+0x1c2);
    }
}
```

El `0x` es el prefijo para que Java interprete el sistema hexadecimal.

El programa nos devuelve `450`.

## Convirtiendo a octal

Hacemos:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        int numero=450;
        System.out.println("Nuestro numero es: "+numero);
        String numeroBinario=Integer.toBinaryString(numero);
        System.out.println("Numero en binario: "+numeroBinario);
        System.out.println("Numero en binario escrito en Java: "+0b111000010);
        System.out.println("Numero en hexadecimal: "+Integer.toHexString(numero));
        System.out.println("Numero en hexadecimal escrito en Java: "+0x1c2);
        System.out.println("Numero en octal: "+Integer.toOctalString(numero));
    }
}
```

El programa nos devuelve `702`.

Para que Java nos lea un número octal:

* Tomamos el código octal del número
* Lo escribimos
* Antes de iniciar, le ponemos un `0`

Ejemplo:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        int numero=450;
        System.out.println("Nuestro numero es: "+numero);
        String numeroBinario=Integer.toBinaryString(numero);
        System.out.println("Numero en binario: "+numeroBinario);
        System.out.println("Numero en binario escrito en Java: "+0b111000010);
        System.out.println("Numero en hexadecimal: "+Integer.toHexString(numero));
        System.out.println("Numero en hexadecimal escrito en Java: "+0x1c2);
        System.out.println("Numero en octal: "+Integer.toOctalString(numero));
        System.out.println("Numero en octal escrito en Java: "+0702);
    }
}
```

El `0` es el prefijo para que Java interprete el sistema octal.

El programa nos devuelve `450`.

## Resumen

Código con comentarios de los prefijos:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        int numero=450;
        System.out.println("Nuestro numero es: "+numero);
        String numeroBinario=Integer.toBinaryString(numero);
        System.out.println("Numero en binario: "+numeroBinario);
        // 0b prefijo para binario
        System.out.println("Numero en binario escrito en Java: "+0b111000010);
        System.out.println("Numero en hexadecimal: "+Integer.toHexString(numero));
        // 0x prefijo para hexadecimal
        System.out.println("Numero en hexadecimal escrito en Java: "+0x1c2);
        // 0 prefijo para octal
        System.out.println("Numero en octal: "+Integer.toOctalString(numero));
        System.out.println("Numero en octal escrito en Java: "+0702);
    }
}
```

Si cambiamos el valor de `numero`, la parte de `escrito en Java` no va a cambiar ya que esta puesta directamente:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        int numero=45;
        System.out.println("Nuestro numero es: "+numero);
        String numeroBinario=Integer.toBinaryString(numero);
        System.out.println("Numero en binario: "+numeroBinario);
        // 0b prefijo para binario
        System.out.println("Numero en binario escrito en Java: "+0b111000010);
        System.out.println("Numero en hexadecimal: "+Integer.toHexString(numero));
        // 0x prefijo para hexadecimal
        System.out.println("Numero en hexadecimal escrito en Java: "+0x1c2);
        // 0 prefijo para octal
        System.out.println("Numero en octal: "+Integer.toOctalString(numero));
        System.out.println("Numero en octal escrito en Java: "+0702);
    }
}
```

Pero el valor de `numero` en los diferentes sistemas numéricos si nos lo devuelve.