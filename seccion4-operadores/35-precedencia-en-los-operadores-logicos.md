# 35. Precedencia en los operadores lógicos

Código de ejemplo:

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

Si tenemos distintas condiciones, las podemos combinar. Es decir, en `r1` podemos poner todo entre paréntesis, de ahí saltarnos a un **o**,
`mentira==false`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores logicos
        int a=7, b=5;
        boolean mentira=false;
        boolean r1= (a>b || a==b)||(mentira==false);
        boolean r2= a>b && mentira==true;
        System.out.println(r1);
        System.out.println(r2);
    }
}
```

Esto nos devolverá `true`. Porque la primera condición devuelve `true`, y si un lado del operador `||` da `true`, devuelve `true`.

Pero en el caso `a<b || a==b`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores logicos
        int a=7, b=5;
        boolean mentira=false;
        boolean r1= (a<b || a==b)||(mentira==false);
        boolean r2= a>b && mentira==true;
        System.out.println(r1);
        System.out.println(r2);
    }
}
```

Sigue dando `true`. Porque `a<b || a==b` es `false`, pero `mentira==false` es `true`.

Pero en el caso `mentira==true`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores logicos
        int a=7, b=5;
        boolean mentira=false;
        boolean r1= (a<b || a==b)||(mentira==true);
        boolean r2= a>b && mentira==true;
        System.out.println(r1);
        System.out.println(r2);
    }
}
```

Esto nos devuelve `false`. Porque ambas condiciones fueron `false`.

Es decir, podemos meter condiciones lógicas dentro de condiciones lógicas para complicarn más el asunto.
Básicamente eso es la parte de precedencia, podemos leer lo que está en paréntesis y le podemos poner un operador en medio de ellos para seguir
comparando cosas, hacer condiciones lógicas mas complicadas cada vez.

Los paréntesis son para no confundirnos, para tener nuestras condiciones lógicas bien establecidas.

Con un **y**, podemos meter todo entre paréntesis, le ponemos un **o** `||`, y ponemos `a==b&&a<b`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores logicos
        int a=7, b=5;
        boolean mentira=false;
        boolean r1= (a<b || a==b)||(mentira==true);
        boolean r2= (a>b && mentira==true)||(a==b&&a<b);
        System.out.println(r1);
        System.out.println(r2);
    }
}
```

Y luego, ponemos paréntesis a todo, ponemos un **y** `&&`, y ponemos `mentira==false`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores logicos
        int a=7, b=5;
        boolean mentira=false;
        boolean r1= (a<b || a==b)||(mentira==true);
        boolean r2= ((a>b && mentira==true)||(a==b&&a<b))&&(mentira==false);
        System.out.println(r1);
        System.out.println(r2);
    }
}
```

Esto nos devuelve `false`. Toda la parte a la izquiera de **y** `&&`, para que sea `true`, todo a la izquierda tiene que ser `true`:

* `a>b` es `true`
* `mentira==true` es `false`
* `a>b && mentira==true` es `false`
* `(a>b && mentira==true)||(a==b&&a<b)` es `false`

Pero si `mentira==false`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores logicos
        int a=7, b=5;
        boolean mentira=false;
        boolean r1= (a<b || a==b)||(mentira==true);
        boolean r2= (a>b && mentira==false)||(a==b&&a<b);
        System.out.println(r1);
        System.out.println(r2);
    }
}
```

Entonces, devuelve `true`. Ambos lados dan `true`.

Los operadores lógicos tienen precedencia, quiere decir que le podemos poner otras operaciones lógicas que las preceden y las tiene que evaluar
antes de evaluar el operador que pusimos después.