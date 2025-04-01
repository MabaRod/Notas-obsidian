# Variables y constantes
1. Char (1 byte) solo guarda un caracter del set local de caracteres
2. int  (2-4 bytes)  guarda un numero natural de tipo entero.
	1. Se puede aplicar short y long 
```
	1. #include <stdio.h>
	2. long m = 12 // se asume que es un entero
	3. short n = 15 // se asume que es un entero
	4. 
```
1. Float (4 bytes) numero singular de punto flotante
2. Double (8 bytes) numero doble de punto flotante

| singed int                                                                                 | Unsigned int                                                                             |
| ------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------- |
| Se pueden usar positivos y negativos                                                       | Solo numeros positivos                                                                   |
| A signed integer can hold values from -232/2 – 1 (-2147483648) to 232/2 – 1 ( 2147483647 ) | A 32-bit unsigned integer can store only positive values from 0 to 232 -1 ( 4294967295 ) |
| A signed integer can get an overflow error while used in a program with larger values.     | Wraps around to 0 if the value exceeds the maximum limit.                                |

### Nomenglatura correcta para variables y constantes
#### Variables
Hay restricciones al nombrar bariables, debe empezar con una letra y el _ cuenta como una letra.  En la practica de C es usar letras minusculas como inicio de variables y MAYUSCULAS para constantes. No se deben usar palabras claves como if, else, for, while, etc.
#### Constantes
##### # Define x 
Un entero largo (long) debe de ser marcado con una L final 123456789L;
Para los numeros de punto flotante  se puede usar notacon cientifica (1e-2). Los sufijos f o F indica una constante de tipo float.

Constante de tipo char es un entero, escrito 'con comillas asi' 
Ciertos characteres pueden ser representado como strings con la linea de scape de \n (usada en la función printf())
### lineas de escape
- \a alerta 
- \b backspace
- \f formfeed
- \n nueva linea
- \r representa la acción de mover el cursor o el cabezal de impresión de regreso al principio de la línea actual.
- \t tabulación horizontal
- \v tabulación vertical
- \ \ backslash
- \ ? simbolo de pregunta
- \ ' quote
- \ " 
- \ooo numero octal
- \xhh numero exhadecimal
### La constante \0
Representa un caracter con valor - que enfatisa el 
### Enum 
Exciste la constante Enum que es de *constante de enumeración*, es una lista de constantes enteros, siguiendo un sistema así, literalmente enumera las cosas

```
#indclude <stdio.h>

int main (){
		enum boolean {no , yes};
	/*   00            1     2  */  
		enum meses { enero = 1, febrero, mar, abril ...}
	/*   00            1            2     3     4  etc. */
	
  }
```

Los Enum deben tener diferentes nombres más no diferentes valores.

