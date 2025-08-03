# 20. Conversiones entre tipos primitivos

## Conversión entre tipos numéricos

### Convirtiendo `int` a `short`

Si tenemos:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        int i=400;
        short s=i;
    }
}
```

Nos dará un error. Y el error que si el valor de `i` que es `int` es muy grande, ya no será compatible con `short`. Para forzarlo haremos algo llamado **casting** o **cast**.

Vamos a forzar que esa variable se vuelva `short`, poniendo el tipo de dato entre paréntesis `()` al lado de la variable a la que queremos hacer igual.

Si hacemos un `sout` a la variable `s`:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        int i=400;
        short s=(short) i;
        System.out.println(s);
    }
}
```

Se ejecutará sin ningún problema.

Si esto lo hacemos y es un número más grande del que `short` puede soportar, vamos a tener algo llamado **pérdida de información**.

### Convirtiendo `int` a `long`

Simplemente hacemos:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        int i=400;
        short s=(short) i;
        System.out.println(s);
        long l=i;
        System.out.println(l);
    }
}
```

`long` no nos causa conflicto, ya que puede soportar un tamaño considerable lo suficiente como para que `int` no le cause conflicto en caso de que crezca.

### Convirtiendo `int` a `char`

Esto:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        int i=400;
        short s=(short) i;
        System.out.println(s);
        long l=i;
        System.out.println(l);
        char c=i;
    }
}
```

Nos causará error, ya que debemos usar el **casting**:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        int i=400;
        short s=(short) i;
        System.out.println(s);
        long l=i;
        System.out.println(l);
        char c=(char) i;
    }
}
```

Y le ponemos `sout`:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        int i=400;
        short s=(short) i;
        System.out.println(s);
        long l=i;
        System.out.println(l);
        char c=(char) i;
        System.out.println(c);
    }
}
```

Esto nos devuelve el símbolo Epsilon (ε), esto es porque `char` interpreta el número como el código de un caracter.