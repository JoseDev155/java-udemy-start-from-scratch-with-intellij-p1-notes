# 31. Operadores Unarios

Pasan un número de negativo a positivo, y de positivo a negativo. Lo hacemos utilizando las leyes de los signos:

* `+ * + = +`
* `+ * - = -`
* `- * + = -`
* `- * - = +`

Código de ejemplo:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores Unarios
    }
}
```

## Convirtiendo a positivo

Por ejemplo, si tenemos un `int` y queremos volverlo positivo, hacemos:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores Unarios
        int i=-2;
        int j= -i;
    }
}
```

Hay que ponerle una separación para que el programa no intente algo que no debería.

Hacemos un `sout` y sacamos `j`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores Unarios
        int i=-2;
        int j= -i;
        System.out.println(j);
    }
}
```

Y nos lo convirtió a positivo, devuelve `2`. Java si interpreta las leyes de los signos.

## Seguir siendo positivo

Ahora, queremos un `int` y queremos que siga siendo positivo, entonces, simplemente sacamos un `int` y hacemos `sout`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores Unarios
        int i=-2;
        int j= -i;
        System.out.println(j);
        int k=4;
        int m= +k;
        System.out.println(m);
    }
}
```

El signo sigue siendo igual, devuelve `4`.

## Seguir siendo negativo

Pero, si fuera `-4`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores Unarios
        int i=-2;
        int j= -i;
        System.out.println(j);
        int k=-4;
        int m= +k;
        System.out.println(m);
    }
}
```

No le cambia el signo, porque el mas `+` simplemente significa multiplicar por un `1`, y el menos `-` significa multiplicar por un `-1`.
Como ya nos tiene acostumbrados la aritmética de números reales.