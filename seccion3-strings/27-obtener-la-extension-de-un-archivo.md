# 27. Obtener la extensión de un archivo

Vamos a resolver un problema:

```java
public class ProgramandoConStrings {
    public static void main(String[] args) {
        String archivo="Imagen_generica.png";
    }
}
```

Tomaremos el `String` `archivo` y queremos sacarle la extensión.

## Obtener el último puntp

Lo que nos indica dónde empieza la extensión del archivo es el punto `.`, pero como puede haber mas puntos, podemos poner:

```java
public class ProgramandoConStrings {
    public static void main(String[] args) {
        String archivo="Imagen_generica.png";
        int i=archivo.lastIndexOf('.');
    }
}
```

Esto nos vsa a guardar en dónde esta puesto el punto.

## Cantidad de caracteres del archivo

Ahora, vamos a necesitar cuántos caracteres tiene el archivo. Ponemos:

```java
public class ProgramandoConStrings {
    public static void main(String[] args) {
        String archivo="Imagen_generica.png";
        int i=archivo.lastIndexOf('.');
        System.out.println(archivo.length());
    }
}
```

Tiene `19` caracteres.

## Obteniendo los caracteres delante del punto con el método `substring()`

Ahora, simplemente vamos a querer quitarle lo que tiene a partir del punto para adelante, vamos a querer el número de caracteres que venga
delante.

Simplemente vamos a utilizar la función `substring()`, vamos a agarrar un subconjunto del `String`. Vamos a poner:

```java
public class ProgramandoConStrings {
    public static void main(String[] args) {
        String archivo="Imagen_generica.png";
        int i=archivo.lastIndexOf('.');
        System.out.println(archivo.length());
        System.out.println(archivo.substring(i));
    }
}
```

Aquín hay un problema, no podemos ponerle simplemente la `i` porque nos devuelve `.png` y necesitamos lo que va después del punto.

Entonces, simplemente le ponemos `i+1`:

```java
public class ProgramandoConStrings {
    public static void main(String[] args) {
        String archivo="Imagen_generica.png";
        int i=archivo.lastIndexOf('.');
        System.out.println(archivo.length());
        System.out.println(archivo.substring(i+1));
    }
}
```

Esto nos devuelve `png`.

Listo, ya obtuvimos la extensión del archivo.

Con `substring()` podemos extraer mucha información a partir de simplemente dónde está parado un punto en un archivo, en un nombre de
archivo.