# 13. Char y caracteres especiales

Veremos algunos de los caracteres especiales o secuencias de escape, en Java.

Son simplemente caracteres que Java interpreta como un carácter, aunque se escriban con mas de uno, pero nos dan cierta funcionalidad a la hora de concatenar caracteres, crear cadenas
de caracteres que serían los `string`'s.

Declaramos otra variable `char`:

```java
char saltoDeLinea='\n';
```

Este es un salto de línea, y con este, cada vez que estemos en un `string` podemos saltar de línea.

Declaramos otra variable `char`:

```java
char retroceso='\b';
```

A la hora de concatenar, se regresa un espacio.

Declaramos otra variable `char`:

```java
char tabulador='\t';
```

Separa palabras con espacio de tabulador.

Declaramos otra variable `char`:

```java
char principioDeLinea='\r';
```

Movernos al principio de la línea actual.

Declaramos otra variable `char`:

```java
char nuevaPagina='\f';
```

Mueve el cursor al principio de la siguiente página.

Declaramos otra variable `char`:

```java
char comillas='\"';
```

Poner comillas en Java. Para cuando hagamos un `string` y queramos ponerle comillas.

Declaramos otra variable `char`:

```java
char comillaSimple='\'';
```

Poner comilla simple.

Declaramos otra variable `char`:

```java
char barraInversa='\\';
```

Poner barra inversa.