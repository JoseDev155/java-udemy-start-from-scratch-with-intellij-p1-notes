# 34. Operadores Lógicos

Hay 2 tipos de operadores, van a ser útiles dentro de los flujos de control.

Código de ejemplo:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores logicos
        int a=7, b=5;
        boolean mentira=false;
    }
}
```

## Operador OR `||`

Vamos a poner otro `boolean`.

Para poner **o** en Java, usamos estas dos barritas `||`, a la izquierda va una sentencia lógica, y a la derecha va otra.

Veremos el caso en el que `a` es menor que `b`, o en el caso en el que `a` es exactamente igual a `b`.

Hacemos `sout`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores logicos
        int a=7, b=5;
        boolean mentira=false;
        boolean r1= a<b || a==b;
        System.out.println(r1);
    }
}
```

Esto nos devuelve `false`. Porque `a<b` es `false`, y `a==b` tampoco es cierto, entonces, eso es `false` siempre.

Un **o** (OR) nos indica de que si 1 de las 2 es **verdadera**, entonces, el `boolean` va a dar **verdadero**. Si las 2 son
**verdaderas**, el `boolean` va a dar **verdadero**. Si las 2 son **falsas**, es **falso**.

Ahora, si en vez de menor `a<b`, le ponemos mayor `a>b`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores logicos
        int a=7, b=5;
        boolean mentira=false;
        boolean r1= a>b || a==b;
        System.out.println(r1);
    }
}
```

Entonces, 1 de las 2 si es cierta, nos devuelve `true`.

Podemos poner las sentencias entre paréntesis, podemos poner entre paréntesis todo, podemos no ponerlo en paréntesis, como queramos.

## Operador AND `&&`

Ponemos:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores logicos
        int a=7, b=5;
        boolean mentira=false;
        boolean r1= a>b || a==b;
        boolean r2= a>b && a==b;
        System.out.println(r1);
    }
}
```

El **y** significa que tienen que pasar ambas cosas, tanto que `a>b` como que `a==b`. Si las 2 pasan, entonces es **verdadero**, si una de las
2 falla, entonces es **falso**. Y si las 2 fallan, es **falso**.

El **o**, con que 1 sea **verdadera**, se vuelve **verdadero**. El **y**, las 2 tienen que ser **verdaderas** para que se vuelva el
`boolean` **verdadero**.

Entonces, hacemos `sout` de `r2`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores logicos
        int a=7, b=5;
        boolean mentira=false;
        boolean r1= a>b || a==b;
        boolean r2= a>b && a==b;
        System.out.println(r1);
        System.out.println(r2);
    }
}
```

Nos devuelve `false`. Porque `a>b` es `true` pero `a==b` es `false`.

También podemos mezclar cosas:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores logicos
        int a=7, b=5;
        boolean mentira=false;
        boolean r1= a>b || a==b;
        boolean r2= a>b && mentira==true;
        System.out.println(r1);
        System.out.println(r2);
    }
}
```

Podemos pedirle cosas en sentido lógico o numérico, y las podemos mezclar en estos operadores. Y no hay ningún problema mientras las
operaciones lógicas estén bien definidas.