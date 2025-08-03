# 10. Primitivos numéricos enteros

Declaramos 3 variables:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        int a=10;
        long b=20;
        byte c=25;
    }
}
```

Si intentamos operar entre ellas:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        int a=10;
        long b=20;
        byte c=25;
        System.out.println("La suma de los tres numeros es: "+(a+b+c));
    }
}
```

Las va sumar sin ningún problema.

Las variables de tipo entero se pueden relacionar entre ellas sin ningún problema. Se pueden sumar, se pueden restar y se pueden multiplicar. Sin embargo, para la división necesitamos
algo más . Si hacemos la división de `a` entre `b`:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        int a=10;
        long b=20;
        byte c=25;
        System.out.println("La suma de los tres numeros es: "+(a+b+c));
	System.out.println(a/b);
    }
}
```

Esto nos dará `0`. O por ejemplo, `c` entre `b`:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        int a=10;
        long b=20;
        byte c=25;
        System.out.println("La suma de los tres numeros es: "+(a+b+c));
	System.out.println(c/b);
    }
}
```

Esto nos dará `1`. Vemos que está redondeando el resultado.

Eso es lo malo de dividir con enteros.

Las variables enteras funcionan cuando queremos crear iteraciones, al contar cosas, y por eso se usan mucho. Pero si queremos utilizar puntos decimales, hacer cálculos mas
avanzados, dividir, tendríamos que usar las variables de punto flotante de tipo numérico.