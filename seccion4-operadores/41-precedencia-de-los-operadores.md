# 41. Precedencia de los operadores

Esto significa básicamente la jerarquía de operaciones en cuanto a los operadores se refiere.

## Ejemplo de promedio

Vamos a hacer un promedio. Vamos a poner 3 números (`a`, `b`, `c`) y una variable `promedio`.

Y ponemos un `sout` de `promedio`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        int a=18;
        int b=15;
        int c=5;

        double promedio=(a+b+c)/3;
        System.out.println(promedio);
    }
}
```

Corremos el programa y nos devuelve `12.0`.

Esto no debería ser muy exacto, esto pasa porque los números no son `double`.

Para decirle a Java que está división de enteros sea en `double`, basta con que uno de ellos sea `double`.

Para hacerlo, cambiamos `3` por `3d`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        int a=18;
        int b=15;
        int c=5;

        double promedio=(a+b+c)/3d;
        System.out.println(promedio);
    }
}
```

Con `d`, estamos especificando que es un `double`.

Esto nos devuelve `12.666666666666666`.

## Operadores `++` y `--`

Ahora, ¿de qué nos sirve hacer el promedio si no estamos utilizando ningún operador? Porque, primero haremos una separación entre los
números:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        int a=18;
        int b=15;
        int c=5;

        double promedio=(a +b +c)/3d;
        System.out.println(promedio);
    }
}
```

Vamos a hacer:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        int a=18;
        int b=15;
        int c=5;

        double promedio=(a++ +b-- +c)/3d;
        System.out.println(promedio);
    }
}
```

Con `a++` vamos a sumar y `b--` vamos a restar, pero no afecta el resultado porque no hace la operación aquí.

Ya que los operadores `a++` y `b--` asignan al valor anterior, le suman y le restan `1` pero después de llamarlo.

Entonces, el resultado tendría que cambiar si lo que hacemos primero es poner `++a`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        int a=18;
        int b=15;
        int c=5;

        double promedio=(++a +b-- +c)/3d;
        System.out.println(promedio);
    }
}
```

Esto nos devuelve `13.0`. Porque a `b--` le quito `1` hasta después de evaluar el `promedio`, y a `a++` le sumó `1` ya justamente cuando lo
evaluamos.
`a` paso de valer `18` a `19`.

Se lee de derecha a izquierda, pero en este caso que hará `--b`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        int a=18;
        int b=15;
        int c=5;

        double promedio=(++a +--b +c)/3d;
        System.out.println(promedio);
    }
}
```

Esto nos devuelve `12.666666666666666`. Porque `--b` restó `1` y `++a` sumó `1`, entonces el resultado se queda igual.

Esto tiene un orden, Java los lee de derecha a izquierda. Con `3d` interpreta que esto es `double`, entonces lo lee como `double`.
Luego, tenemos `c`, `--b`, `++a`, como es un precedente, osea, antes de ejecutar el `promedio`, pues lo hace antes.
Y ahora si ejecuta todo, y listo, nos devuelve el `promedio`.

Más o menos esa es la idea de la precedencia con operadores en Java.