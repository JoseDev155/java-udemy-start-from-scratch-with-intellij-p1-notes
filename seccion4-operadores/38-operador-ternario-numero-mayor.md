# 38. Operador Ternario Número mayor

Veremos la misma estructura `if-else`, pero la diremos de otra forma para poder resolver el problema con operadores ternarios de que si
introducimos 3 números, cuál es el mayor de ellos.

Usaremos el mismo programa de la clase anterior:

```java
import java.util.Scanner;

public class ProgramandoConOperadores {
    public static void main(String[] args) {
        Scanner entrada=new Scanner(System.in);
        System.out.println("INGRESA TU CALIFICACION DEL PARCIAL");
        double u=entrada.nextDouble();

        if (u<6) {
            System.out.println("ESTAS REPROBADO");
        } else {
            System.out.println("ESTAS APROBADO");
        }
    }
}
```

Borramos el `if-else`, y ponemos:

```java
import java.util.Scanner;

public class ProgramandoConOperadores {
    public static void main(String[] args) {
        Scanner entrada=new Scanner(System.in);
        System.out.println("INTRODUCE EL PRIMER NUMERO");
        double a=entrada.nextDouble();
        System.out.println("INTRODUCE EL SEGUNDO NUMERO");
        double b=entrada.nextDouble();
        System.out.println("INTRODUCE EL TERCER NUMERO");
        double c=entrada.nextDouble();
    }
}
```

Modificamos las variables a `int`, ya que vamos a utilizar una nueva forma de hacer esta clase de operaciones.

Esto para que no haya interpretaciones de si un número en fracción es más grande que otro:

```java
import java.util.Scanner;

public class ProgramandoConOperadores {
    public static void main(String[] args) {
        Scanner entrada=new Scanner(System.in);
        System.out.println("INTRODUCE EL PRIMER NUMERO");
        int a=entrada.nextInt();
        System.out.println("INTRODUCE EL SEGUNDO NUMERO");
        int b=entrada.nextInt();
        System.out.println("INTRODUCE EL TERCER NUMERO");
        int c=entrada.nextInt();
    }
}
```

Ahora, vamos a definir un nuevo `int`:

```java
import java.util.Scanner;

public class ProgramandoConOperadores {
    public static void main(String[] args) {
        Scanner entrada=new Scanner(System.in);
        System.out.println("INTRODUCE EL PRIMER NUMERO");
        int a=entrada.nextInt();
        System.out.println("INTRODUCE EL SEGUNDO NUMERO");
        int b=entrada.nextInt();
        System.out.println("INTRODUCE EL TERCER NUMERO");
        int c=entrada.nextInt();

        int max;
    }
}
```

No está inicializado.

Ahora, vamos a poner una expresión lógica, es decir, vamos a ver si `a` es mayor que `b`, si el primer número es mayor que el otro, vamos a preguntarle `?` a Java si esto pasa, entonces, vamos a definir a `max` como `a`:

```java
import java.util.Scanner;

public class ProgramandoConOperadores {
    public static void main(String[] args) {
        Scanner entrada=new Scanner(System.in);
        System.out.println("INTRODUCE EL PRIMER NUMERO");
        int a=entrada.nextInt();
        System.out.println("INTRODUCE EL SEGUNDO NUMERO");
        int b=entrada.nextInt();
        System.out.println("INTRODUCE EL TERCER NUMERO");
        int c=entrada.nextInt();

        int max;
        max=(a>b)? a:b;
    }
}
```

Esta expresión se lee de la siguiente manera: estamos declarando, asignando y metiendo un `if`. Si `a>b`, si es cierto, entonces devuelve
`a`, si no es cierto devuelve `b`.
Para eso es este operador ternario.

Y ahora, necesitamos comparar este resultado con el tercer número:

```java
import java.util.Scanner;

public class ProgramandoConOperadores {
    public static void main(String[] args) {
        Scanner entrada=new Scanner(System.in);
        System.out.println("INTRODUCE EL PRIMER NUMERO");
        int a=entrada.nextInt();
        System.out.println("INTRODUCE EL SEGUNDO NUMERO");
        int b=entrada.nextInt();
        System.out.println("INTRODUCE EL TERCER NUMERO");
        int c=entrada.nextInt();

        int max;
        max=(a>b)? a:b;
        max=(max>c)? max:c;
    }
}
```

Si el `max` que encontramos anteriormente, es mayor que `c`, si es cierto devuelve `max`, si no es cierto devuelve `c` como máximo.

Y ponemos `sout`:

```java
import java.util.Scanner;

public class ProgramandoConOperadores {
    public static void main(String[] args) {
        Scanner entrada=new Scanner(System.in);
        System.out.println("INTRODUCE EL PRIMER NUMERO");
        int a=entrada.nextInt();
        System.out.println("INTRODUCE EL SEGUNDO NUMERO");
        int b=entrada.nextInt();
        System.out.println("INTRODUCE EL TERCER NUMERO");
        int c=entrada.nextInt();

        int max;
        max=(a>b)? a:b;
        max=(max>c)? max:c;
        System.out.println("EL MAXIMO ENTRE LOS TRES NUMEROS ES: "+max);
    }
}
```

Funciona correctamente.

Si ponemos números iguales, devolverá 1 de los 2 que son iguales. Devuelve todo sin problema.

Lógicamente esta bien argumentado la expresión lógica que tenemos ahí.