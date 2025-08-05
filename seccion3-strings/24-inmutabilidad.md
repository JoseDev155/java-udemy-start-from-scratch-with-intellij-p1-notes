# 24. Inmutabilidad

**NOTA IMPORTANTE**: Seguiremos trabajndo con el código de la clase pasada.

Se dice que un `String` es **inmutable**, porque es ajeno a que le podamos modificar cosas una vez declarado (a menos que usemos ciertas
instancias de la clase `String`).

Por ejemplo, si ya no quisieramos declarar tanta concatenación y quisieramos concatenar igual pero modificando el `String` original, en
este caso, queremos modificar el `String` `Saludo`, hacemos la misma concatenación usando el método `transform()`.

## Modificando con el método `transform()`

El método `transform()` nos pide una función para devolvernos el `String`. Entonces, ponemos en este caso `s` para no seguir usando `Saludo`, una flecha y abrimos corchetes `{}`:

```java
public class ProgramandoConStrings {
    public static void main(String[] args) {
        String Saludo="Hola, gracias por la información ";
        String Nombre="Abraham";
        String SaludoPersonalizado=Saludo+"querido "+Nombre;
        String SaludoPersonalizado2=Saludo.concat("querido ").concat(Nombre);
        System.out.println(SaludoPersonalizado);
        System.out.println(SaludoPersonalizado2);

        Saludo=Saludo.transform(s -> {
            
        });
    }
}
```

Ahora, `s` que es nuestro `String` `Saludo`, será enviado adentro de la función, y debemos retornar un valor:

```java
public class ProgramandoConStrings {
    public static void main(String[] args) {
        String Saludo="Hola, gracias por la información ";
        String Nombre="Abraham";
        String SaludoPersonalizado=Saludo+"querido "+Nombre;
        String SaludoPersonalizado2=Saludo.concat("querido ").concat(Nombre);
        System.out.println(SaludoPersonalizado);
        System.out.println(SaludoPersonalizado2);

        Saludo=Saludo.transform(s -> {
            return s+"querido "+Nombre;
        });
    }
}
```

Esto transformó a `Saludo` (para transformar a `Saludo` tuvimos que hacer todo lo anterior), mandamos `s` que es nuestro `Saludo` y
retornamos el nuevo valor.

Ahora, hacemos `sout` de `Saludo`:

```java
public class ProgramandoConStrings {
    public static void main(String[] args) {
        String Saludo="Hola, gracias por la información ";
        String Nombre="Abraham";
        String SaludoPersonalizado=Saludo+"querido "+Nombre;
        String SaludoPersonalizado2=Saludo.concat("querido ").concat(Nombre);
        System.out.println(SaludoPersonalizado);
        System.out.println(SaludoPersonalizado2);

        Saludo=Saludo.transform(s -> {
            return s+"querido"+Nombre;
        });
        System.out.println(Saludo);
    }
}
```

Esto nos devolverá el `String` concatenado. Esta es otra forma de concatenar `String`'s.

## Reemplazando dentro de un `String` con `replace()`

Nos podría interesar reemplazar las `a` por otra mayúscula.

Ahora, nos vamos a `Nombre` y queremos cambiar las `a` minúsculas por `A` mayúsculas.

Entonces, hacemos `replace()` y nos dirá que necesitamos 2 `char`, en este caso vamos a reemplazar las `a` minúsculas por `A` mayúsculas:

```java
public class ProgramandoConStrings {
    public static void main(String[] args) {
        String Saludo="Hola, gracias por la información ";
        String Nombre="Abraham";
        String SaludoPersonalizado=Saludo+"querido "+Nombre;
        String SaludoPersonalizado2=Saludo.concat("querido ").concat(Nombre);
        System.out.println(SaludoPersonalizado);
        System.out.println(SaludoPersonalizado2);

        Saludo=Saludo.transform(s -> {
            return s+"querido"+Nombre;
        });
        System.out.println(Saludo);
        Nombre=Nombre.replace("a", "A");
    }
}
```

Esto toma 2 argumentos, el argumento que queremos quitar, y lo reemplazamos por lo que queremos.

Ahora, hacemos `sout` de `Nombre`:

```java
public class ProgramandoConStrings {
    public static void main(String[] args) {
        String Saludo="Hola, gracias por la información ";
        String Nombre="Abraham";
        String SaludoPersonalizado=Saludo+"querido "+Nombre;
        String SaludoPersonalizado2=Saludo.concat("querido ").concat(Nombre);
        System.out.println(SaludoPersonalizado);
        System.out.println(SaludoPersonalizado2);

        Saludo=Saludo.transform(s -> {
            return s+"querido"+Nombre;
        });
        System.out.println(Saludo);
        Nombre=Nombre.replace("a", "A");
        System.out.println(Nombre);
    }
}
```

Esto nos dará error, ya que `Nombre` ya lo estamos reemplazando, pero va aparte como una variable a referencia. Entonces, creamos una variable
igual a `Nombre` y a esta variable si le podemos hacer todo lo que hicimos anteriormente:

```java
public class ProgramandoConStrings {
    public static void main(String[] args) {
        String Saludo="Hola, gracias por la información ";
        String Nombre="Abraham";
        String Nombre1="Abraham";
        String SaludoPersonalizado=Saludo+"querido "+Nombre;
        String SaludoPersonalizado2=Saludo.concat("querido ").concat(Nombre);
        System.out.println(SaludoPersonalizado);
        System.out.println(SaludoPersonalizado2);

        Saludo=Saludo.transform(s -> {
            return s+"querido"+Nombre;
        });
        System.out.println(Saludo);

        Nombre1=Nombre1.replace("a", "A");
        System.out.println(Nombre1);
    }
}
```

Esto nos devuelve `AbrAhAm`.

Tanmbién, vimos que si ya usamos una variable dentro de una función flecha, se vuelve una **variable temporal**:

```java
Saludo=Saludo.transform(s -> {
    return s+"querido"+Nombre;
});
```

Por eso ya no podíamos usar `Nombre`, se vuelve una variable temporal o una instancia temporal para nuestro código.

Porque `tranform()` concatena, pero los transforma y los une. Se vuelve como constante, por eso el error decía que se volvió `final`.