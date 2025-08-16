# 33. Operadores Relacionales

Nos sirven para relacionar 2 variables primitivas.

Código de ejemplo:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores relacionales

    }
}
```

Vamos a poner unas variables `int`:

Código de ejemplo:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores relacionales
        int a=7, b=5;
    }
}
```

## Operador de igualdad estricta `==`

Los relacionales son de tipo `boolean`, entonces, pondremos `relacional 1` va a ser igual a una expresión. La pondremos entre paréntesis `()`
para no perder orden en lo que vamos a hacer, y le ponemos `sout`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores relacionales
        int a=7, b=5;
        boolean r1= (a==b);
        System.out.println(r1);
    }
}
```

Los números deben ser iguales para que devuelva `true`. En este caso, nos devuelve `false`.

## Operador de negación `=!`

Vamos a negar el resultado:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores relacionales
        int a=7, b=5;
        boolean r1= (a==b);
        System.out.println(r1);
        boolean r2= !r1;
    }
}
```

Con esto negamos el valor de `r1`. Si tenemos:

* **Falso**, su negación es **verdadero**
* **Verdadero**, su negación es **falso**

En este caso, como `r1` es `false`, su negación es `true`. Si hacemos `sout` de `r2`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores relacionales
        int a=7, b=5;
        boolean r1= (a==b);
        System.out.println(r1);
        boolean r2= !r1;
        System.out.println(r2);
    }
}
```

Nos devuelve `true`. Los `boolean`'s se comportan bien con las operaciones lógicas.

En los `string`'s, usamos `.equals()`.

## Operador distinto que `!=`

Vamos a poner:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores relacionales
        int a=7, b=5;
        boolean r1= (a==b);
        System.out.println(r1);
        boolean r2= !r1;
        System.out.println(r2);
        boolean r3= (a!=b);
    }
}
```

Esto es cierto, debería devolvernos `true`. Así escribimos que algo es distinto de algo.

Hacemos `sout` de `r3`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores relacionales
        int a=7, b=5;
        boolean r1= (a==b);
        System.out.println(r1);
        boolean r2=!r1;
        System.out.println(r2);
        boolean r3= (a!=b);
        System.out.println(r3);
    }
}
```

Esto nos devuelve `true`.

## Operador de igualdad estricta `==` con `boolean`'s

Declaramos un `boolean`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores relacionales
        int a=7, b=5;
        boolean mentira=false;
        boolean r1= (a==b);
        System.out.println(r1);
        boolean r2=!r1;
        System.out.println(r2);
        boolean r3= (a!=b);
        System.out.println(r3);
        boolean r4= (true==mentira);
    }
}
```

Hacemos `sout` de `r4`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores relacionales
        int a=7, b=5;
        boolean mentira=false;
        boolean r1= (a==b);
        System.out.println(r1);
        boolean r2=!r1;
        System.out.println(r2);
        boolean r3= (a!=b);
        System.out.println(r3);
        boolean r4= (true==mentira);
        System.out.println(r4);
    }
}
```

Y nos devuelve `false`. Esto operador también funciona con variables lógicas.

## Operador distinto que `!=` con `boolean`'s

Ponemos:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores relacionales
        int a=7, b=5;
        boolean mentira=false;
        boolean r1= (a==b);
        System.out.println(r1);
        boolean r2=!r1;
        System.out.println(r2);
        boolean r3= (a!=b);
        System.out.println(r3);
        boolean r4= (true==mentira);
        System.out.println(r4);
        boolean r5= (true!=mentira);
    }
}
```

Hacemos `sout` de `r5`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores relacionales
        int a=7, b=5;
        boolean mentira=false;
        boolean r1= (a==b);
        System.out.println(r1);
        boolean r2=!r1;
        System.out.println(r2);
        boolean r3= (a!=b);
        System.out.println(r3);
        boolean r4= (true==mentira);
        System.out.println(r4);
        boolean r5= (true!=mentira);
        System.out.println(r5);
    }
}
```

Esto nos devuelve `true`.

## Operador menor que `<`

Ponemos:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores relacionales
        int a=7, b=5;
        boolean mentira=false;
        boolean r1= (a==b);
        System.out.println(r1);
        boolean r2=!r1;
        System.out.println(r2);
        boolean r3= (a!=b);
        System.out.println(r3);
        boolean r4= (true==mentira);
        System.out.println(r4);
        boolean r5= (true!=mentira);
        System.out.println(r5);
        boolean r6= (a<b);
    }
}
```

Hacemos `sout` de `r6`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores relacionales
        int a=7, b=5;
        boolean mentira=false;
        boolean r1= (a==b);
        System.out.println(r1);
        boolean r2=!r1;
        System.out.println(r2);
        boolean r3= (a!=b);
        System.out.println(r3);
        boolean r4= (true==mentira);
        System.out.println(r4);
        boolean r5= (true!=mentira);
        System.out.println(r5);
        boolean r6= (a<b);
        System.out.println(r6);
    }
}
```

Esto nos devuelve `false`

## Operador mayor que `>`

Ponemos:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores relacionales
        int a=7, b=5;
        boolean mentira=false;
        boolean r1= (a==b);
        System.out.println(r1);
        boolean r2=!r1;
        System.out.println(r2);
        boolean r3= (a!=b);
        System.out.println(r3);
        boolean r4= (true==mentira);
        System.out.println(r4);
        boolean r5= (true!=mentira);
        System.out.println(r5);
        boolean r6= (a<b);
        System.out.println(r6);
        boolean r7= (a>b);
    }
}
```

Hacemos `sout` de `r7`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores relacionales
        int a=7, b=5;
        boolean mentira=false;
        boolean r1= (a==b);
        System.out.println(r1);
        boolean r2=!r1;
        System.out.println(r2);
        boolean r3= (a!=b);
        System.out.println(r3);
        boolean r4= (true==mentira);
        System.out.println(r4);
        boolean r5= (true!=mentira);
        System.out.println(r5);
        boolean r6= (a<b);
        System.out.println(r6);
        boolean r7= (a>b);
        System.out.println(r7);
    }
}
```

Esto nos devuelve `true`.

Ahora, si le quitamos los paréntesis `()` a `r7`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores relacionales
        int a=7, b=5;
        boolean mentira=false;
        boolean r1= (a==b);
        System.out.println(r1);
        boolean r2=!r1;
        System.out.println(r2);
        boolean r3= (a!=b);
        System.out.println(r3);
        boolean r4= (true==mentira);
        System.out.println(r4);
        boolean r5= (true!=mentira);
        System.out.println(r5);
        boolean r6= (a<b);
        System.out.println(r6);
        boolean r7= a>b;
        System.out.println(r7);
    }
}
```

Sigue funcionando igual, Java es indiferente, a menos de que no los peguemos. Si están indentados, si les ponemos un espacio, Java los
interpreta perfectamente pero si no se los ponemos, podemos caer en un conflicto de que lee primero Java, etc.

Para evitar problemas, mejor ocupamos paréntesis.

La mayoría de operadores relacionales van dentro de argumentos, para hacer algún tipo de flujo de control, algún tipo de proceso, dentro de
una función, etc.

## Operador menor o igual que `<=`

Ponemos:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores relacionales
        int a=7, b=5;
        boolean mentira=false;
        boolean r1= (a==b);
        System.out.println(r1);
        boolean r2=!r1;
        System.out.println(r2);
        boolean r3= (a!=b);
        System.out.println(r3);
        boolean r4= (true==mentira);
        System.out.println(r4);
        boolean r5= (true!=mentira);
        System.out.println(r5);
        boolean r6= (a<b);
        System.out.println(r6);
        boolean r7= a>b;
        System.out.println(r7);
        boolean r8= a<=b;
    }
}
```

Hacemos `sout` de `r8`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores relacionales
        int a=7, b=5;
        boolean mentira=false;
        boolean r1= (a==b);
        System.out.println(r1);
        boolean r2=!r1;
        System.out.println(r2);
        boolean r3= (a!=b);
        System.out.println(r3);
        boolean r4= (true==mentira);
        System.out.println(r4);
        boolean r5= (true!=mentira);
        System.out.println(r5);
        boolean r6= (a<b);
        System.out.println(r6);
        boolean r7= (a>b);
        System.out.println(r7);
        boolean r8= a<=b;
        System.out.println(r8);
    }
}
```

Esto nos devuelve `false`.

## Operador mayor o igual que `>=`

Ponemos:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores relacionales
        int a=7, b=5;
        boolean mentira=false;
        boolean r1= (a==b);
        System.out.println(r1);
        boolean r2=!r1;
        System.out.println(r2);
        boolean r3= (a!=b);
        System.out.println(r3);
        boolean r4= (true==mentira);
        System.out.println(r4);
        boolean r5= (true!=mentira);
        System.out.println(r5);
        boolean r6= (a<b);
        System.out.println(r6);
        boolean r7= (a>b);
        System.out.println(r7);
        boolean r8= a<=b;
        System.out.println(r8);
        boolean r9= a>=b;
    }
}
```

Hacemos `sout` de `r9`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores relacionales
        int a=7, b=5;
        boolean mentira=false;
        boolean r1= (a==b);
        System.out.println(r1);
        boolean r2=!r1;
        System.out.println(r2);
        boolean r3= (a!=b);
        System.out.println(r3);
        boolean r4= (true==mentira);
        System.out.println(r4);
        boolean r5= (true!=mentira);
        System.out.println(r5);
        boolean r6= (a<b);
        System.out.println(r6);
        boolean r7= (a>b);
        System.out.println(r7);
        boolean r8= a<=b;
        System.out.println(r8);
        boolean r9= a>=b;
        System.out.println(r9);
    }
}
```

Esto nos devuelve `true`.