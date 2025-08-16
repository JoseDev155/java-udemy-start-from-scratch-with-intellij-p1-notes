# 37. Operador Ternario

Usaremos el mismo programa de la clase anterior:

```java
import java.util.Scanner;

public class ProgramandoConOperadores {
    public static void main(String[] args) {
        String usuario="Abraham";
        String contraseña="12345";
        Scanner entrada=new Scanner(System.in);
        System.out.println("INTRODUCE TU NOMBRE DE USUARIO");
        String u=entrada.nextLine();
        System.out.println("INTRODUCE TU CONTRASEÑA");
        String p=entrada.nextLine();

        if (usuario.equals(u)&&contraseña.equals(p)) {
            System.out.println("DATOS AUTENTICADOS. BIENVENIDO");
        } else {
            System.out.println("DATOS ERRONEOS, INTENTE DE NUEVO");
        }
    }
}
```

Vamos a hacerle una pequeña modificación a este programa, para que ahora haga otra cosa con respecto a los operadores ternarios.

Vamos a hacer un programa que nos diga si un alumno esta aprobado o esta reprobado.

Quitamos los `String`'s, ponemos "**INGRESA TU CALIFICACION DEL PARCIAL**". Quitamos el `sout` y la variable `p`.
En esta caso, no queremos un `String`, queremos un `double`, tendremos un conflicto porque debemos cambiar `nextLine()` por `nextDouble()`.

Quitamos lo que hay el paréntesis del `if`, y ponemos, si `u` o la calificación sea mayor o igual a `6`, entonces diremos
"**ESTAS APROBADO**", y si no pasa eso, le decimos "**ESTAS REPROBADO**":

```java
import java.util.Scanner;

public class ProgramandoConOperadores {
    public static void main(String[] args) {
        Scanner entrada=new Scanner(System.in);
        System.out.println("INGRESA TU CALIFICACION DEL PARCIAL");
        double u=entrada.nextDouble();

        if (u>=6) {
            System.out.println("ESTAS APROBADO");
        } else {
            System.out.println("ESTAS REPROBADO");
        }
    }
}
```

Esto es lo que hacen los operadores ternarios, es decir, mayor o igual, y si no, haces otra cosa.

Pero estos operadores tienen un montón de aplicaciones. Si queremos decir "**ESTAS APROBADO**", pero lo queremos escribir de otra forma.

Si ponemos la condición `u<6`, ponemos:

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

Es otra forma de escribir este programa.