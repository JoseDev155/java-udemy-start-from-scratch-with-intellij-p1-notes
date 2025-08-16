# 28. Introducción a los operadores

## Operadores

Un operador lleva a cabo operaciones sobre uno (operador *unario*), dos (operador *binario*) o tres (operador *binario*) datos u *operandos* de
tipo primitivo devolviendo un valor determinado también de un tipo primitivo.
El tipo de valor devuelto tras la evaluación depende del operador y del tipo de los operandos.

## Operador de asignación

| Operador | Descripción         | Ejemplo de expresión | Resultado del ejemplo |
| -------- | ------------------- | -------------------- | --------------------- |
| `=`      | Operador asignación | `n = 4`              | `n` vale `4`          |

Con este operador podemos asignar variables.

## Operadores aritméticos

| Operador | Descripción                        | Ejemplo de expresión   | Resultado del ejemplo |
| -------- | ---------------------------------- | ---------------------- | --------------------- |
| `-`      | operador unario de cambio de signo | `-4`                   | `-4`                  |
| `+`      | Suma                               | `2.5 + 7.1`            | `9.6`                 |
| `-`      | Resta                              | `235.6 - 103.5`        | `132.1`               |
| `*`      | Producto                           | `1.2 * 1.1`            | `1.32`                |
| `/`      | División (tanto entera como real)  | `0.050 / 0.2`<br>`7/2` | `0.25`<br>`3`         |
| `%`      | Resto de la división entera        | `20 + 7`               | `6`                   |

Todo lo relacionado a porque sirve el **resto** se llama **aritmética modular** y es una parte muy importante de la programación.
Si queremos saber cuántos números primos hay, o queremos programas que busquen números primos, o programas que busquen ciertos números
específicos con ciertas características, y a veces utilizar los **restos** a la hora de dividir es bastante importante.

## Operadores aritméticos incrementales

| Operador | Descripción                        | Ejemplo de expresión   | Resultado del ejemplo |
| -------- | ---------------------------------- | ---------------------- | --------------------- |
| `++`     | Incremento<br>`i++` primero se utiliza la variable y luego se incrementa su valor<br>`++i` primero se incrementa el valor de la variable y luego se utiliza | `4++`<br>`a=5;`<br>`b=a++;`<br>`a=5;`<br>`b=++a;` | `5`<br><br>`a` vale `6` y `b` vale `5`<br><br>`a` vale `6` y `b` vale `6` |
| `--`     | decremento        | `4--`               | `3`                   |

## Operadores aritméticos combinados

| Operador | Descripción        | Ejemplo de expresión | Resultado del ejemplo |
| -------- | ------------------ | -------------------- | --------------------- |
| `+=`     | Suma combinada     | `a+=b`               | `a=a+b`               |
| `-=`     | Resta combinada    | `a-=b`               | `a=a-b`               |
| `*=`     | Producto combinado | `a*=b`               | `a=a*b`               |
| `/=`     | División combinada | `a/=b`               | `a=a/b`               |
| `%=`     | Resto combinado    | `a%=b`               | `a=a%b`               |

## Operadores de relación

| Operador | Descripción       | Ejemplo de expresión | Resultado del ejemplo |
| -------- | ----------------- | -------------------- | --------------------- |
| `==`     | igual que         | `7 == 38`            | `false`               |
| `!=`     | distinto que      | `'a' != 'k'`         | `true`                |
| `<`      | menor que         | `'G' < 'B'`          | `false`               |
| `>`      | mayor que         | `'b' > 'a'`          | `true`                |
| `<=`     | menor o igual que | `7.5 <= 7.38`        | `false`               |
| `>=`     | mayor o igual que | `38 >= 7`            | `true`                |

## Operadores lógicos o booleanos

| Operador | Descripción                           | Ejemplo de expresión                 | Resultado del ejemplo |
| -------- | ------------------------------------- | ------------------------------------ | --------------------- |
| `!`      | Negación - NOT (unario)               | `!false`<br>`!(5==5)`                | `true`<br>`false`     |
| `\|`     | Suma lógica - OR (binario)            | `true \| false`<br>`(5==5) \| (5<4)` | `true`<br>`true`      |
| `^`      | Suma lógica exclusiva - XOR (binario) | `true ^ false`<br>`(5==5) \| (5<4)`  | `true`<br>`true`      |
| `&`      | Producto lógico - AND (binario)       | `true & false`<br>`(5==5) & (5<4)`   | `false`<br>`false`    |
| `\|\|`   | Suma lógica con cortocircuito: si el primer operando es `true` entonces el segundo se salta y el resultado es `true` | `true \|\| false`<br>`(5==5) \|\| (5<4)` | `true`<br>`true`      |
| `&&`     | Producto lógico con cortocircuito: si el primer operando es `false` entonces el segundo se salta y el resultado es `false` | `false && true`<br>`(5==5) && (5<4)` | `false`<br>`false`    |