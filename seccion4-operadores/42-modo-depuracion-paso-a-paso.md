# 42. Modo depuración paso a paso

A veces, vamos a querer ver paso a paso como va corriendo nuestro programa y ver exactamente dónde está un error en cuanto a nuestra
programación.

Para hacer esto, en lugar de correr nuestro programa o todo el programa, y ya que el programa nos diga en que falló, pues irlo corriendo línea a
línea.

Para esto sirve el Modo **Debug** o **Debugging**.

Para activarlo, nos vamos a una **línea de quiebre**, es decir, a una línea que nos interese para iniciar nuestro Debug.

Usaremos el mismo programa de la clase anterior:

```java
import java.util.Scanner;

public class ProgramandoConOperadores {
    public static void main(String[] args) {
        int a=18;
        int b=15;
        int c=5;

        double promedio=(++a +--b +c)/3d;
        System.out.println(promedio);
    }
}
```

## Haciendo Debug en nuestro programa

Hacemos clic en la línea que queremos, en este caso en la línea `6`. Hacemos clic al lado del número y veremos que se pone en rojo, eso
significa que la hemos marcado para ser nuestra línea de quiebre.

Ahora, para entrar al Modo Debug, hay 2 formas, podemos entrar en lugar de darle clic a **Run**, al lado le damos a **Debug** que tiene forma de
insecto.

Nos va a pedir un acceso privado para redes, y listo.

Nos abre una nueva ventana dentro del programa que dice **Debug**, nos dice que entramos en `main` y que no hay problema y corrió esta
`public class` (`ProgramandoConOperadores`), toda esta parte del `static void` y todo.

Para correr la siguiente línea, nos vamos al botón que dice **Step Over**, y va a leer la primera línea que simplemente es:

```plaintext
a = 18
```

Después, que lea la siguiente línea, qu e lea la siguiente:

```plaintext
a = 18
b = 15
c = 5
```

Después, que lea el `promedio`:

```plaintext
a = 19
b = 14
c = 5
promedio = 12.666666666666666
```

Y como veremos en el archivo `ProgrmandoConOperadores.java`, aparece toda la información de las variables, cómo son declaradas, cuál fue su
`promedio`. Todo esto comentado sin ningún problema y nos va dando detalle a detalle todo lo que va pasando con nuestro programa.

Y ahora simplemente terminó el programa y nos enseña bien dondé están las llaves `{}`, y cerró el `main`. Y con eso se acabó el **Debugging**.

Volvemos a entrar a nuestro Modo **Debug** para verlo de nuevo. Pasamos al siguiente paso con **Step Over**, si queremos **Step Into**, es decir,
seguir bajando. En este caso, el **Step Into** es para seguir bajando pero dentro de instancias o de métodos en específico.

Tenemos **Force Step Into**, osea, que aunque hay un error sigue bajando. O **Step Out**, es decir, un paso más por arriba, o salirse del
método en este caso.