# 32. Operadores de Incremento y Decremento

Cuando veamos flujos de control, estos operadores en específico van a ser muy útiles porque nos van a ayudar mucho a la hora de hacer
iteraciones, crear procesos, hacer operaciones que requieran de que un valor vaya subiendo o bajando de uno en uno.

Código de ejemplo:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores Aritmeticos de incremento y decremento

        // Incrementa en uno y luego devuelve el numero


        // Devuelve el numero y luego incrementa uno


        // Decrementa en uno y luego devuelve el numero


        // Devuelve el numero y luego decrementa en uno
        
    }
}
```

Hay dos tipos de operadores aritméticos de ese tipo:

* Pre-incremento
* Post-incremento

Para hacer esto, vamos a declarar primero un `int`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores Aritmeticos de incremento y decremento
        int a=5;
        // Incrementa en uno y luego devuelve el numero


        // Devuelve el numero y luego incrementa uno


        // Decrementa en uno y luego devuelve el numero


        // Devuelve el numero y luego decrementa en uno
        
    }
}
```

## Incrementa en uno y luego devuelve el número

Vamos a poner:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores Aritmeticos de incremento y decremento
        int a=5;
        // Incrementa en uno y luego devuelve el numero
        int b=++a;
        System.out.println(b);

        // Devuelve el numero y luego incrementa uno


        // Decrementa en uno y luego devuelve el numero


        // Devuelve el numero y luego decrementa en uno
        
    }
}
```

Es un pre-incremento, `a` incrementa en `1`, ahora es `6`. Y luego devuelve el número incrementado.

## Devuelve el número y luego incrementa uno

Ejemplo:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores Aritmeticos de incremento y decremento
        int a=5;
        // Incrementa en uno y luego devuelve el numero
        int b=++a;
        System.out.println(b);

        // Devuelve el numero y luego incrementa uno
        int c=a++;
        System.out.println(c);

        // Decrementa en uno y luego devuelve el numero


        // Devuelve el numero y luego decrementa en uno

    }
}
```

Esto nos va a seguir dando `6`, porque va a devolver el número y luego va a incrementar `1`.

Si sacamos el `a++` de aquí, directamente es lo que nos va a dar.

Ambos parecen iguales, pero son distintos entre ellos a la hora que trabajamos con ellos.

Porque a la hora que lo metemos a un programa, lo que hará el programa es considerar primero a `a` y después le sube el valor.

## Decrementa en uno y luego devuelve el número

Así mismo tenemos también para resta:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores Aritmeticos de incremento y decremento
        int a=5;
        // Incrementa en uno y luego devuelve el numero
        int b=++a;
        System.out.println(b);

        // Devuelve el numero y luego incrementa uno
        int c=a++;
        System.out.println(c);

        // Decrementa en uno y luego devuelve el numero
        int d=--a;
        System.out.println(d);

        // Devuelve el numero y luego decrementa en uno

    }
}
```

Esto nos devuelve `6`, ya que en el código anterior le sumamos `1` y ahora le restamos `1`.

Para verlo más claro, reiniciamos el valor de `a`, ya que está haciendo las operaciones pero las está concatenando y eso no está bien:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores Aritmeticos de incremento y decremento
        int a=5;
        // Incrementa en uno y luego devuelve el numero
        int b=++a;
        System.out.println(b);

        // Devuelve el numero y luego incrementa uno
        a=5;
        int c=a++;
        System.out.println(c);

        // Decrementa en uno y luego devuelve el numero
        a=5;
        int d=--a;
        System.out.println(d);

        // Devuelve el numero y luego decrementa en uno

    }
}
```

Ahora, ya tenemos las diferencias. Entonces:

* `b=++a`: Le sumó `1` y después nos lo devolvió
* `c=a++`: Nos devuelve `5`, el número original y después le suma el número. Si quisieramos sacar a `c` otra vez sería distinto
* `d=--a`: Decrementa en `1` y devuelve `4`. Es un pre-decremento

## Devuelve el número y luego decrementa en uno

Volvemos a reiniciar `a` y hacemos:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores Aritmeticos de incremento y decremento
        int a=5;
        // Incrementa en uno y luego devuelve el numero
        int b=++a;
        System.out.println(b);

        // Devuelve el numero y luego incrementa uno
        a=5;
        int c=a++;
        System.out.println(c);

        // Decrementa en uno y luego devuelve el numero
        a=5;
        int d=--a;
        System.out.println(d);

        // Devuelve el numero y luego decrementa en uno
        a=5;
        int e=a--;
        System.out.println(e);
    }
}
```

Nos va a seguir dando `5` porque lo decremento después.

Si volvemos a hacer `sout`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores Aritmeticos de incremento y decremento
        int a=5;
        // Incrementa en uno y luego devuelve el numero
        int b=++a;
        System.out.println(b);

        // Devuelve el numero y luego incrementa uno
        a=5;
        int c=a++;
        System.out.println(c);

        // Decrementa en uno y luego devuelve el numero
        a=5;
        int d=--a;
        System.out.println(d);

        // Devuelve el numero y luego decrementa en uno
        a=5;
        int e=a--;
        System.out.println(e);
        System.out.println(e);
    }
}
```

Seguimos teniendo `5` porque aún no lo ha decrementado. Pero con `a`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores Aritmeticos de incremento y decremento
        int a=5;
        // Incrementa en uno y luego devuelve el numero
        int b=++a;
        System.out.println(b);

        // Devuelve el numero y luego incrementa uno
        a=5;
        int c=a++;
        System.out.println(c);

        // Decrementa en uno y luego devuelve el numero
        a=5;
        int d=--a;
        System.out.println(d);

        // Devuelve el numero y luego decrementa en uno
        a=5;
        int e=a--;
        System.out.println(e);
        System.out.println(a);
    }
}
```

Su valor es `4` porque ya lo decrementó en `1`. Es un post-decremento. Al que le afecta estas cosas es a `a`.

En el caso `a++`, `c` vale `5` pero después, si hacemos `sout` de `a`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores Aritmeticos de incremento y decremento
        int a=5;
        // Incrementa en uno y luego devuelve el numero
        int b=++a;
        System.out.println(b);

        // Devuelve el numero y luego incrementa uno
        a=5;
        int c=a++;
        System.out.println(c);
        System.out.println(a);

        // Decrementa en uno y luego devuelve el numero
        a=5;
        int d=--a;
        System.out.println(d);

        // Devuelve el numero y luego decrementa en uno
        a=5;
        int e=a--;
        System.out.println(e);
        System.out.println(a);
    }
}
```

Nos devuelve `6`, porque ya le sumó `1`. Es un post-incremento.