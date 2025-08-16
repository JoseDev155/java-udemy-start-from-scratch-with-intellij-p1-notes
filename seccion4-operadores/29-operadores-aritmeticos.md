# 29. Operadores Aritméticos

## **NOTA IMPORTANTE**: Nuevo proyecto

Se creo un nuevo proyecto llamado `ProgramandoConOperadores`:

```plaintext
Project name: ProgramandoConOperadores
Project location: C:\Users\usuario\IdeaProjects\ProgramandoConOperadores
```

Dentro del `src/` del proyecto creamos una clase llamada `ProgramandoConOperadores.java`:

```java
public class ProgramandoConOperadores {
}
```

Ejecutamos `psvm` para crear el método `main()` y agregamos un comentario:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores Aritmeticos
    }
}
```

## Suma

Para hacer esto, vamos a agarrar 2 números enteros y vamos a efectuar la suma:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores Aritmeticos
        int a,b;
        int suma=a+b;
    }
}
```

Esto nos marcará rojo, porque `a` y `b` no están inicializadas, es decir, que no tienen un valor.

## Resta

Vamos a hacer otro `int`, vamos a poner:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores Aritmeticos
        int a,b;
        int suma=a+b;
        int resta=a-b;
    }
}
```

## Multiplicación

Vamos a poner un `int`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores Aritmeticos
        int a,b;
        int suma=a+b;
        int resta=a-b;
        int multiplicacion=a*b;
    }
}
```

## División

Y un:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores Aritmeticos
        int a,b;
        int suma=a+b;
        int resta=a-b;
        int multiplicacion=a*b;
        int division=a/b;
    }
}
```

## Inicializando las variables

El valor por defecto de las variables sería `0`. Les vamos a poner:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores Aritmeticos
        int a=5,b=7;
        int suma=a+b;
        int resta=a-b;
        int multiplicacion=a*b;
        int division=a/b;
    }
}
```

Vamos a tener un problema en `division`, porque no podemos convertir `a/b` a flotante. Sin embargo, ¿qué pasaría si forzamos el valor de `a` y
`b` para que sean flotantes, y así volver la división a un flotante?

Entonces, haremos directamente poner `float`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores Aritmeticos
        int a=5,b=7;
        int suma=a+b;
        int resta=a-b;
        int multiplicacion=a*b;
        float division=(float)a/(float)b;
    }
}
```

## Resto

Vamos a utilizar el último que es `int`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores Aritmeticos
        int a=5,b=7;
        int suma=a+b;
        int resta=a-b;
        int multiplicacion=a*b;
        float division=(float)a/(float)b;
        int resto= a%b;
    }
}
```

## Imprimiendo por pantalla

Ponemos `sout`:

```java
public class ProgramandoConOperadores {
    public static void main(String[] args) {
        // Operadores Aritmeticos
        int a=5,b=7;
        int suma=a+b;
        int resta=a-b;
        int multiplicacion=a*b;
        float division=(float)a/(float)b;
        int resto= a%b;
        System.out.println("suma= "+suma);
        System.out.println("resta= "+resta);
        System.out.println("multiplicacion= "+multiplicacion);
        System.out.println("division= "+division);
        System.out.println("resto= "+resto);
    }
}
```

Y el programa nos devuelve:

```plaintext
suma= 12
resta= -2
multiplicacion= 35
division= 0.71428573
resto= 5
```