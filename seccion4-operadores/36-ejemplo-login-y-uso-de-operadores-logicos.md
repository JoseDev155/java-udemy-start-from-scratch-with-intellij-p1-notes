# 36. Ejemplo Login y uso de operadores lógicos

Vamos a programar un Login, vamos a pedirle al usuario su nombre de usuario, su contraseña, vamos a verificarla con una que ya tenemos
preestablecida y vamos a decirle si entra o no entra.

Lo vamos a hacer con un `if-else`, una estructura lógica.

## Username y contraseña

Lo primero que vamos a hacer es predeterminar nuestro username y nuestra contraseña.

Primero necesitamos 2 `String`'s:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        String usuario="Abraham";
        String contrasena="12345";
    }
}
```

## Escáner

Necesitamos un **escáner** porque le vamos a pedir al usuario los datos.

Entonces, vamos a poner:

```java
import java.util.Scanner;

public class ProgramandoConOperadores {
    public static void main(String[] args) {
        String usuario="Abraham";
        String contraseña="12345";
        Scanner entrada=new Scanner(System.in);
    }
}
```

Ahora, le decimos con un `sout` al usuario:

```java
import java.util.Scanner;

public class ProgramandoConOperadores {
    public static void main(String[] args) {
        String usuario="Abraham";
        String contraseña="12345";
        Scanner entrada=new Scanner(System.in);
        System.out.println("INTRODUCE TU NOMBRE DE USUARIO");
    }
}
```

Y ahora vamos a poner lo que sea que ingrese, se va a guardar en una nueva variable. Entonces, vamos a ponerle:

```java
import java.util.Scanner;

public class ProgramandoConOperadores {
    public static void main(String[] args) {
        String usuario="Abraham";
        String contraseña="12345";
        Scanner entrada=new Scanner(System.in);
        System.out.println("INTRODUCE TU NOMBRE DE USUARIO");
        String u=entrada.nextLine();
    }
}
```

Ahora, vamos a pedir la contraseña. Hacemos un `sout` y abrimos otro `String`:

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
    }
}
```

Tanto `u` como `p` quedan definidas con lo que sea que introduzcamos. Para verificar que esto pasa, usaremos la estructura lógica `if-else`.

## `ìf-else`

Si ocurre lo que metamos en los 2 paréntesis `()`, en este caso, verificar que `usuario` sea exactamente igual (`equals()`) a `u`. Pero
también queremos verificar otra cosa, el `equals()` dice **verdadero** o **falso**, entonces, queremos que tenga que pasar exclusivamente las 2
cosas al mismo tiempo, necesitamos el operador lógico **y** `&&`, y vamos a poner que `contraseña.equals()`, `p`.
Es decir, queremos que verifique si tanto el `usuario` como la `contraseña` son iguales a `u` y `p`, exactamente iguales, caracter por
caracter, entonces, lo que vaya dentro de las llaves `{}` es lo que va a hacer el programa:

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
            
        }
    }
}
```

Si esto ocurre, quiere decir que vamos a ponerle:

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
        }
    }
}
```

Si no ocurre, vamos a ponerle `else`, y como ya estamos diciendo la otra posibilidad le ponemos un `sout`:

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

Esto funciona correctamente.