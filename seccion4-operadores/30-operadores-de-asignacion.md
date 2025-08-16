# 30. Operadores de Asignación

Estos operadores aritméticos nos dan una forma de escribir de forma corta y bastante efectiva, ciertas cosas que nos podrían ayudar en la
hora de hacer nuestro código.

Código de ejemplo:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores Aritmeticos de Asignacion
    }
}
```

Si tenemos un `int`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores Aritmeticos de Asignacion
        int i=5;
    }
}
```

Y queremos irle sumando `2` a cada iteración, una forma de hacerlo sería:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores Aritmeticos de Asignacion
        int i=5;
        int j=i+2;
    }
}
```

Y hacer esta operación una y otra vez. Pero Java, nos da una forma muy interesante de hacerlo.

Entonces, vamos a renombrar a nuestra variable `i` y le vamos a sumar el `2`, directamente con un solo comando.

## Operador `+=`

Vamos a poner un `sout` y vamos a poner:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores Aritmeticos de Asignacion
        int i=5;
        int j=i+2;
        i+=2;
        System.out.println(i);
    }
}
```

Esta expresión `i+=2`, podría resultar ser bastante sencilla. Sin embargo, esto oculta lo que tenemos arriba.

Esto nos devuelve `7`. Estamos asignando un nuevo valor para `i`, aparte de su valor anterior.

Se puede hacer otra vez, con otra expresión. con otro número después de esto. Le vamos a sumar `5` y le ponemos un `sout`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores Aritmeticos de Asignacion
        int i=5;
        int j=i+2;
        i+=2;
        System.out.println(i);
        i+=5;
        System.out.println(i);
    }
}
```

Ahora es `12`.

También hay para resta, multiplicación y división.

## Operador `-=`

Ahora le vamos a restar `4` y le ponemos `sout`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores Aritmeticos de Asignacion
        int i=5;
        int j=i+2;
        i+=2;
        System.out.println(i);
        i+=5;
        System.out.println(i);
        i-=4;
        System.out.println(i);
    }
}
```

Esto es cuando queremos hacer operaciones iterativas a nuestros números.

Esto nos devuelve `8`.

## Operador `*=`

Ahora, le queremos multiplicar por `3` y hacemos `sout`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores Aritmeticos de Asignacion
        int i=5;
        int j=i+2;
        i+=2;
        System.out.println(i);
        i+=5;
        System.out.println(i);
        i-=4;
        System.out.println(i);
        i*=3;
        System.out.println(i);
    }
}
```

Estamos concatenando operaciones.

Esto nos da `24`.