# 11. Primitivos numéricos de punto flotante

Se dividen en `double` y `float`.

## Declarando variable `float`

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        float variable=2.5f;
    }
}
```

## Diferencias entre `float` y `double`

`float` se apoya de la aritmética del punto flotante. Una serie de reglas y convenciones matemáticas para poder poner el punto decimal de cierta forma.

Haremos un `sout` para poder ver la salida de esto:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        float variable=2.5f;
        System.out.println(variable);
    }
}
```

Esto nos devolverá `2.5`.

Con la `f` le estamos diciendo al programa que utilice la notación decimal normal.

`float` está hecho para la notación científica. A la hora que vamos a cambiar de sistemas numéricos, `float` nos ayudará.

¿Para qué cambiar de sistemas numéricos? Por ejemplo, el sistema **hexadecimal** sirve para temas de ángulos, sistemas de numeración, tiempo, entre otros.

Si queremos más decimales, en el caso de querer transformar `2.5` en `25` o `250`, lo multiplicaríamos por `10^n`. En este caso, lo multiplicaremos por `10^2`:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        float variable=2.5e2f;
        System.out.println(variable);
    }
}
```

Esto nos devolverá `250.0`. `e` nos indica la potencia de `10` que queremos utilizar y `2` que es el exponente.

## Declarando variable `double`

Si queremos usar decimales comunes, usamos el tipo `double`:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        float variable=2.5e2f;
        System.out.println(variable);
        double variable2=2.67;
        System.out.println(variable2);
    }
}
```

Esto nos devolverá `2.67`.