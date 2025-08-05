# 21. Introducción a los String

Es un tipo de dato referencial a objeto. Están compuestos por caracteres y se usan con comillas dobles `""`.

## Características

* Tipo de dato referencial a objeto
 * Inmutables
 * Se concatenan con el operador suma: `+`
 * Con el operador `==` se comparan por referencia
 * Con el operador `equals()` se compara por valor

## Métodos más importantes

# Métodos más importantes

| MÉTODO             | DESCRIPCIÓN                                                                                     | PARÁMETRO                                                                          | TIPO DE DATO DEVUELTO                      |
|--------------------|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|--------------------------------------------|
| charAt             | Devuelve el carácter indicado por parámetro.                                                    | Un parámetro `int`                                                                  | `char`                                     |
| compareTo          | Sirve para comparar cadenas, devuelve un número según el resultado. Recuerda que no sigue el alfabeto español, lo compara según la tabla ASCII.           | Un parámetro `String`, la cadena a comparar.                                       | `int` <br> - Si devuelve un número mayor que `0`: la primera cadena es mayor que la segunda. <br><br> - Si devuelve un `0`: las cadenas son iguales.<br><br> - Si devuelve un número menor que `0`: la primera cadena es menor que la segunda |
| compareToIgnoreCase| Es igual que el anterior, pero ignorando mayúsculas o minúsculas.                                  | Un parámetro `String`, la cadena a comparar                                       | `int` <br> - Si devuelve un número mayor que `0`: la primera cadena es mayor que la segunda. <br><br> - Si devuelve un `0`: las cadenas son iguales.<br><br> - Si devuelve un número menor que `0`: la primera cadena es menor que la segunda |
| concat             | Concatena dos cadenas, como el operador `+`.                                                    | Un parámetro `String`, la cadena a concatenar                                     | Un nuevo `String` con las cadenas concatenadas.         |
| copyValueOf        | Crea un nuevo `String` a partir de un array de `char`. Este método debe invocarse de manera estática, es decir, `String.copyValueOf(array_char)`.                              | Un array de `char`                                                                 | `String`                                   |
| endsWith           | Indica si la cadena acaba con el `String` pasado por parámetro.                                 | `String`                                                                            | `boolean`                                  |
| equals             | Indica si una cadena es igual que otra.                                                         | `String`                                                                            | `boolean`                                  |
| equalsIgnoreCase   | Es igual que el anterior, pero ignorando mayúsculas o minúsculas.                                  | `String`                                                                            | `boolean`                                  |
| getBytes           | Devuelve un array de bytes con el código ASCII de los caracteres que forman el `String`.       | Ningún parámetro                                                                    | Un array de `bytes`                        |
| indexOf            | Devuelve la posición en la cadena pasada por parámetro desde el principio. `-1` si no existe.                        | `String` o `char`                                                                   | `int`                                      |
| indexOf            | Igual que el anterior, pero además le indicamos la posición desde donde empezamos a buscar.                       | `String` o `char`, el segundo parámetro es un `int`                                          | `int`                                      |
| lastIndexOf        | Devuelve la posición en la cadena pasada por parámetro desde el final. `-1` si no existe.                                         | `String` o `char`                                                                   | `int`                                      |
| lastIndexOf        | Igual que el anterior, pero ademas le indicamos la posición desde donde empezamos a buscar.                              | `String` o `char`, el segundo parámetro es un `int`                                          | `int`                                      |
| length             | Devuelve la longitud de la cadena.                                                              | Ningún parámetro                                                                    | `int`                                      |
| matches            | Indica si la cadena cumple con la expresión pasada como parámetro. Pincha aquí para tener mas detalles.                             | `String`                                                                            | `boolean`                                  |
| replace            | Devuelve un `String` cambiando los caracteres que nosotros le indiquemos.                                        | Dos parámetros `char`, el primero es el carácter que existe en el `String` y el segundo por el que queremos cambiar.                       | `String`                                   |
| replaceFirst       | Devuelve un `String` intercambiando solo la primera coincidencia.                              | Dos parámetros `String`, el primero son los caracteres que existe en el `String` y el segundo por el que queremos cambiar.                                   | `String`                                   |
| replaceAll         | Devuelve un `String` intercambiando todas las coincidencias que se encuentren.                                    | Dos parámetros `String`, el primero son los caracteres que existe en el `String` y el segundo por el que queremos cambiar.                                   | `String`                                   |
| startsWith         | Indica si la cadena empieza por una cadena pasada por parámetro.                                | `String`                                                                            | `boolean`                                  |
| substring          | Trocea un `String` desde una posición a otra.                                                   | Dos parámetros `int`, indica desde dónde empieza hasta donde acaba, este ultimo no se incluye.                         | `String`                                   |
| toCharArray        | Devuelve un array de `char`, todos los caracteres de una `String`.                                 | Ningún parámetro                                                                    | Un array de `char`                         |
| toLowerCase        | Convierte el `String` a minúsculas.                                                             | Ningún parámetro                                                                    | `String`                                   |
| toUpperCase        | Convierte el `String` a mayúsculas.                                                             | Ningún parámetro                                                                    | `String`                                   |
| trim               | Elimina los espacios del `String`.                                                              | Ningún parámetro                                                                    | `String`                                   |
