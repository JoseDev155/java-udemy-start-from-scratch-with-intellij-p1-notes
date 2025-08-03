# 17. Sistemas numéricos y entradas de datos desde el terminal

Usaremos el mismo programa de la clase anterior, pero quitaremos los `JOptionPane` y el `import`:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        System.out.println("Nuestro numero es: "+numeroReal);
        String numeroBinario=Integer.toBinaryString(numeroReal);
        System.out.println("Numero en binario: "+numeroBinario);
        System.out.println("Numero en hexadecimal: "+Integer.toHexString(numeroReal));
        System.out.println("Numero en octal: "+Integer.toOctalString(numeroReal));
        String resultados="Nuestro numero es: "+numeroReal+"\nNumero en hexadecimal: "+Integer.toHexString(numeroReal)+"\nNumero en binario: "+numeroBinario+"\nNumero en octal: "+Integer.toOctalString(numeroReal);
    }
}
```

## `Scanner`

La librería de Java que nos ayudará para esto es la librería `Scanner`. La importamos:

```java
import java.util.Scanner;
```

Cuando la librería no está siendo usada, IntelliJ la marca de color gris.

Vamos a crear un objeto tipo `Scanner`, es decir, un objeto que nos va aceptar la entrada de la computadora cuando lo llamemos.

El tipo de entrada que escogeremos para enteros es `nextInt()`.

También, quitamos la variable `resultados`:

```java
import java.util.Scanner;

public class EjemplosVariables {
    public static void main(String[] args) {
        Scanner entrada=new Scanner(System.in);
        System.out.println("Introduce un numero entero: ");
        int numeroReal=entrada.nextInt();
        System.out.println("Nuestro numero es: "+numeroReal);
        String numeroBinario=Integer.toBinaryString(numeroReal);
        System.out.println("Numero en binario: "+numeroBinario);
        System.out.println("Numero en hexadecimal: "+Integer.toHexString(numeroReal));
        System.out.println("Numero en octal: "+Integer.toOctalString(numeroReal));
    }
}
```

Si ejecutamos nuestro programa e ingresamos un número entero en la consola, veremos que nuestro programa sigue funcionando.