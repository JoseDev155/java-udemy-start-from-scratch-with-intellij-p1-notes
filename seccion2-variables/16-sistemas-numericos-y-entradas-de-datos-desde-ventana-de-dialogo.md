# 16. Sistemas numéricos y entradas de datos desde ventana de dialogo

Quitaremos los `sout` con números directamente puestos y los comentarios del código anterior:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        int numero=45;
        System.out.println("Nuestro numero es: "+numero);
        String numeroBinario=Integer.toBinaryString(numero);
        System.out.println("Numero en binario: "+numeroBinario);
        System.out.println("Numero en hexadecimal: "+Integer.toHexString(numero));
        System.out.println("Numero en octal: "+Integer.toOctalString(numero));
        System.out.println("Numero en octal escrito en Java: "+0702);
    }
}
```

## Abriendo un panel de escritura en Java

Por panel de escritura, nos referimos a una ventana emergente con un mensaje y con la posibilidad de ingresar algo.

Para eso, cambiamos `int` por `String` a la variable `numero` y usamos `JOptionPane.showInputDialog()`.

Está función tiene dos argumentos, el primer argumento no nos importa, por eso vamos a poner `null`, y el segundo argumento es el mensaje:

```java
import javax.swing.*;

public class EjemplosVariables {
    public static void main(String[] args) {
        String numero=JOptionPane.showInputDialog(null, "Ingresa un numero entero: ");
        System.out.println("Nuestro numero es: "+numero);
        String numeroBinario=Integer.toBinaryString(numero);
        System.out.println("Numero en binario: "+numeroBinario);
        System.out.println("Numero en hexadecimal: "+Integer.toHexString(numero));
        System.out.println("Numero en octal: "+Integer.toOctalString(numero));
        System.out.println("Numero en octal escrito en Java: "+0702);
    }
}
```

Al poner `JOptionPane`, automáticamente se nos hace el `import` de la librería en la parte de arriba.

Ahora, también tenemos errores en el código, ya que necesitamos el programa lea a `numero` como un `int`. Si hacemos esto:

```java
numero=Integer.parseInt(numero);
```

Nos dará error, porque la variable ya está declarada. Entonces, hacemos lo siguiente:

```java
import javax.swing.*;

public class EjemplosVariables {
    public static void main(String[] args) {
        String numero=JOptionPane.showInputDialog(null, "Ingresa un numero entero: ");
        int numeroReal=Integer.parseInt(numero);
        System.out.println("Nuestro numero es: "+numeroReal);
        String numeroBinario=Integer.toBinaryString(numeroReal);
        System.out.println("Numero en binario: "+numeroBinario);
        System.out.println("Numero en hexadecimal: "+Integer.toHexString(numeroReal));
        System.out.println("Numero en octal: "+Integer.toOctalString(numeroReal));
        System.out.println("Numero en octal escrito en Java: "+0702);
    }
}
```

Si ejecutamos el programa, nos aparecerá la ventana emergente por pantalla, si ingresamos un número entero, el programa nos devuelve en la consola las conversiones del número en los
diferentes sistemas numéricos.

También eliminamos el `sout` de "**Numero en octal escrito en Java**":

```java
import javax.swing.*;

public class EjemplosVariables {
    public static void main(String[] args) {
        String numero=JOptionPane.showInputDialog(null, "Ingresa un numero entero: ");
        int numeroReal=Integer.parseInt(numero);
        System.out.println("Nuestro numero es: "+numeroReal);
        String numeroBinario=Integer.toBinaryString(numeroReal);
        System.out.println("Numero en binario: "+numeroBinario);
        System.out.println("Numero en hexadecimal: "+Integer.toHexString(numeroReal));
        System.out.println("Numero en octal: "+Integer.toOctalString(numeroReal));
    }
}
```

Si queremos devolver los resultados directamente, hacemos algún concatenado. Para eso usamos un `String` y los caracteres especiales. Devolvemos los resultados en un
`JOptionPane.showMessageDialog()`:

```java
import javax.swing.*;

public class EjemplosVariables {
    public static void main(String[] args) {
        String numero=JOptionPane.showInputDialog(null, "Ingresa un numero entero: ");
        int numeroReal=Integer.parseInt(numero);
        System.out.println("Nuestro numero es: "+numeroReal);
        String numeroBinario=Integer.toBinaryString(numeroReal);
        System.out.println("Numero en binario: "+numeroBinario);
        System.out.println("Numero en hexadecimal: "+Integer.toHexString(numeroReal));
        System.out.println("Numero en octal: "+Integer.toOctalString(numeroReal));
        String resultados="Nuestro numero es: "+numeroReal+"\nNumero en hexadecimal: "+Integer.toHexString(numeroReal)+"\nNumero en binario: "+numeroBinario+"\nNumero en octal: "+Integer.toOctalString(numeroReal);
        JOptionPane.showMessageDialog(null, resultados);
    }
}
```

Esto nos devolverá los resultados en una ventana emergente.