# 23. Concatenando String

Quitaremos las variables `Hola1` y `Hola3`, y los `sout` del código anterior:

```java
public class ProgramandoConStrings {
    public static void main(String[] args) {
        String Hola="Hola, gracias por la información";
    }
}
```

Y renombramos la variable `Hola` por `Saludo`:

```java
public class ProgramandoConStrings {
    public static void main(String[] args) {
        String Saludo="Hola, gracias por la información";
    }
}
```

## Concatenando con `+`

Creamos dos `String`'s nuevos, y le agregamos un espacio a `Saludo`. Luego, hacemos un `sout`:

```java
public class ProgramandoConStrings {
    public static void main(String[] args) {
        String Saludo="Hola, gracias por la información ";
        String Nombre="Abraham";
        String SaludoPersonalizado=Saludo+Nombre;
        System.out.println(SaludoPersonalizado);
    }
}
```

## Concatenando con el método `concat()`

Hay otra forma de concatenar `String`'s, en vez de hacer `SaludoPersonalizado`, podemos hacer:

```java
public class ProgramandoConStrings {
    public static void main(String[] args) {
        String Saludo="Hola, gracias por la información ";
        String Nombre="Abraham";
        String SaludoPersonalizado=Saludo+Nombre;
        String SaludoPersonalizado2=Saludo.concat(Nombre);
        System.out.println(SaludoPersonalizado);
    }
}
```

Lo que estamos usando es la clase/objeto `String` y hacemos uso del del método `concat()`.

Ahora, si le queremos poner algo en medio o concatenar más todavía, ponemos otro `concat()`. Y hacemos un `sout` de `SaludoPersonalizado2`:

```java
public class ProgramandoConStrings {
    public static void main(String[] args) {
        String Saludo="Hola, gracias por la información ";
        String Nombre="Abraham";
        String SaludoPersonalizado=Saludo+Nombre;
        String SaludoPersonalizado2=Saludo.concat("querido ").concat(Nombre);
        System.out.println(SaludoPersonalizado);
        System.out.println(SaludoPersonalizado2);
    }
}
```

Esto es útil por si queremos concatenar cosas predefinidas o un poco más automatizadas.

## Concatenando `String`'s directamente

Ponemos el `String` directamente:

```java
public class ProgramandoConStrings {
    public static void main(String[] args) {
        String Saludo="Hola, gracias por la información ";
        String Nombre="Abraham";
        String SaludoPersonalizado=Saludo+"querido "+Nombre;
        String SaludoPersonalizado2=Saludo.concat("querido ").concat(Nombre);
        System.out.println(SaludoPersonalizado);
        System.out.println(SaludoPersonalizado2);
    }
}
```

Concatenar con `+` y con `concat()` es totalmente equivalente.