# 14. Primitivo boolean o lógico binario

Simplemente almacena un tipo de información: **verdadero** o **falso**.

Declarando variable `boolean`:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        boolean condicion=true;
    }
}
```

O también podríamos ponerle:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        boolean condicion=false;
    }
}
```

El tipo `boolean` sirve para verificar si una condición es cierta o no.

Por ejemplo, ponemos:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        boolean condicion=true;
	boolean verificar= 3==2+1;
    }
}
```

Este `boolean` va a guardar la información, es decir, va a verificar que esta operación sea cierta (el `==` es un **operador lógico**), si es cierta devolvemos `true`, si es falso
devolvemos `false`.

Haremos un `sout` de `verificar`:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        boolean condicion=true;
        boolean verificar= 3==2+1;
        System.out.println(verificar);
    }
}
```

Esto nos devuelve `true`.

Si ponemos algo que no es cierto:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        boolean condicion=true;
        boolean verificar= 4==2+1;
        System.out.println(verificar);
    }
}
```

Nos devuelve `false`.

Esto nos sirve cuando abrimos flujos de control, `if`, `else`, necesitamos verificar condiciones: "si esto pasa, entonces pasa esto".

Esta es una condición lógica y para eso esta hecho el tipo de dato `boolean`.