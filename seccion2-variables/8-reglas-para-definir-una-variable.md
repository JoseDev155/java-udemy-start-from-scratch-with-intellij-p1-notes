# 8. Reglas para definir una variable

Borramos el código que hicimos en la clase pasada.

## Convenciones

1. Comienza el nombre de tu variable siempre con una letra, y además, nunca usar acentos:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        int edad=7;
    }
}
```

2. Los nombres de las variables distinguen entre mayúsculas y minúsculas:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        int edad=7;
        int Edad=9;
        System.out.println(edad);
        System.out.println(Edad);
    }
}
```

Cuando imprimimos, ambos valores son diferentes.

3. Usa nombres descriptivos: Ayuda a documentar el código y saber que hace nuestro código en cada parte.

4. El nombre de tu variable no debe coincidir con alguna palabra reservada: Hay varias palabras reservadas que podemos buscar en el **JAVA LANGUAGE KEYWORDS**.

5. Usa el estilo de escritura **CamelCase** para nombrar tus variables:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        int edad=7;
        int Edad=9;
        System.out.println(edad);
        System.out.println(Edad);
        double indiceMasaCorporal=22;
    }
}
```

6. Si tu variable almacena un valor constante, escribe su nombre completamente con mayúsculas:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        int edad=7;
        int Edad=9;
        System.out.println(edad);
        System.out.println(Edad);
        double indiceMasaCorporal=22;
	double PI=3.14159;
    }
}
```

Y si se compone de más de una palabra:

```java
public class EjemplosVariables {
    public static void main(String[] args) {
        int edad=7;
        int Edad=9;
        System.out.println(edad);
        System.out.println(Edad);
        double indiceMasaCorporal=22;
	double VALOR_PI=3.14159;
    }
}
```