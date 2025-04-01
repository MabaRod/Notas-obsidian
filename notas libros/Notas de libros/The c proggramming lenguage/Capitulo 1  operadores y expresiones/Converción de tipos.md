## converciónes automaticas
Hay operaciones que se convierten de manera automatica al compilar, hay casos que convierten datos más estrechos a datos más achos.
"Hay expreciones que no hacen sentido como convertir un numero de punto flotante a un entero, si bien no son ilegales, solo darán una advertencia"

### Otros ejemplos
"Un caractér no es más que un entero pequeño, perfectamente pueden ser utilizadas para operaciones aritemticas" Para esto mismo exciste la funcion [[Atoi() ]]que es parte de [[<stdlib.h>]]

### Cosas a notar
Es importanet denotar que los numeros de punto flotante no se convierten automaticamente a doubles, en general funciones de la librearia [[<Math.h>]] van a usar doubles en autmotatico ya que necesitan mayor precición

### Converciones en operaciones relacionales
Las reglas de converción son muy complicadas, en parte dependen al tamaño de los datos, si suponemos que un entero es de 16 bits y un long es de 32 bits entoches -1L<1U porque 1U, que es un entero, se convierte en un log asignado. PERO -1L > 1UL porque -1L es convertido en un unsinged long y por lo tanto aparentemente se convierte en un numero positivo largo.

#### ¿Porque?
Basicamente para poder acomodar datos en las computadoras, considerando que las computadoras de cuando C fue creado no tenian tando poder, se necesitan este tipo de optimisaciones para poder funcionar.
``` Ejemplo 
	int i;
	char c;
i = c;
c = i;
El valor de c nocambia. 