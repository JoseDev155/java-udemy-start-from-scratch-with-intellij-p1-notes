# 6. Introducción a las variables

## Tipos de variables

* **Primitivas**: Int, short, byte, long, boolean, float, double

* **Referenciales a Objetos**: Strings, arreglos, etc.

## Variables Primitivas

| Tipo    | Representación / Valor                                | Tamaño (en bits) | Valor mínimo                    | Valor máximo                    | Valor por defecto |
|---------|--------------------------------------------------------|------------------|----------------------------------|----------------------------------|-------------------|
| boolean | true o false                                           | 1                | N.A.                             | N.A.                             | false             |
| char    | Carácter Unicode                                       | 16               | \u0000                           | \uFFFF                           | \u0000            |
| byte    | Entero con signo                                       | 8                | -128                             | 127                              | 0                 |
| short   | Entero con signo                                       | 16               | -32,768                          | 32,767                           | 0                 |
| int     | Entero con signo                                       | 32               | -2,147,483,648                   | 2,147,483,647                    | 0                 |
| long    | Entero con signo                                       | 64               | -9,223,372,036,854,775,808       | 9,223,372,036,854,775,807        | 0                 |
| float   | Coma flotante de precisión simple (Norma IEEE 754)     | 32               | ±3.40282347E+38                  | ±1.40239846E-45                  | 0.0               |
| double  | Coma flotante de precisión doble (Norma IEEE 754)      | 64               | ±1.79769313486231570E+308        | ±4.94065645841246544E-324        | 0.0               |
