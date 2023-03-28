# Ejercicios con Algoritmos

## Primeros 3 Ejercicios

### Ejercicio 1

*Calcular la letra del DNI Español*

**Paso 1:** Definir el problema, a partir de un numero de DNI hemos de calcular la letra

¿Cómo se calcula la letra del DNI?

Número de DNI dividirlo en 23 y el resto será el ```resultadoResto```

El ```resultadoResto``` lo compararemos con la lista de códigos

| resultadoResto | Letra |
| -------------- | ----- |
| 0              | T     |
| 1              | R     |
| 2              | W     |
| 3              | A     |
| 4              | G     |
| 5              | M     |
| 6              | Y     |
| 7              | F     |
| 8              | P     |
| 9              | D     |
| 10             | X     |
| 11             | B     |
| 12             | N     |
| 13             | J     |
| 14             | Z     |
| 15             | S     |
| 16             | Q     |
| 17             | V     |
| 18             | H     |
| 19             | L     |
| 20             | C     |
| 21             | K     |
| 22             | E     |

**Paso 2:** Poner la entrada, el proceso y la salida

Entrada: ``DNI`` ,``tablaLetrasDNI`` ,  ``resultado`` <-""

Proceso: 

- Validar que el DNI tenga 8 digitos y que sean todos numéricos
  - Si es erronea asigne a la variable ``resultado`` "DNI Invalido"

- Dividimos DNI en 23 y el resto lo asignamos a ```resultadoResto```
- Comparar el ``resultadoResto`` con los valores de la tabla, y asignar a ``resultado`` el valor equivalente en la tabla.

Salida:

- Escribir ``resultado``

**Paso 3:** Escribir el pseudocódigo

```
Algoritmo CalculoDNI
# Entrada
DNI<-leerDelTeclado()
tablaLetrasDNI<-"TRWAGMYFPDXBNJZSQVHLCKE"
resultado<-""
# Proceso
Si DNI es valido Entonces # Como validamos 8 digitos y todos numericos
	resultadoResto<-DNI mod 23 #mod es el resto de dividir
	# resultado<-recuperarLetra(resultadoResto,tablaLetrasDNI)
	
	Repetir
	Hasta que "lleguemos hasta 22" 
	
Sino
	resultado<-"DNI Invalido"
Fin Si
# Salida
escribirAlaPantalla(resultado)
Fin Algoritmo
```

      Leer DNI
    	nuevoDNI<-DNI / 10
      Si longitud DNI > 8 o longitud DNI < 8 Entonces
          resultado <- "DNI inválido"

  Mientras longitud DNI > 8 o longitud DNI < 8

#### Prueba del algoritmo

DNI: 36982589

resultado:b,"S"

resultadoResto:15

tablaLetrasDNI: "TRWAGMYFPDXBNJZSQVHLCKE"

S



### Ejercicio 2

*Calcular el salario de un empleado*

**Paso 1:** Definir el problema

**Calcular** el **salario** neto mensual es sencillo. Basta con conocer los datos salariales y personales del trabajador, aplicar los impuestos que deben descontarse del **salario** bruto anual, restarlos al **salario** bruto anual y posteriormente dividir ese importe final entre 12 o 14, en función del número de pagas.

**Paso 2:** Poner la entrada, el proceso y la salida

Entrada: ```salarioBase```, ``pagasExtras``, ``complementos``, ``otrosConceptosRetributivos``

``IRP``, ``Seguridad Social``

Proceso:

Sumar ```salarioBase```, ``pagasExtras``, ``complementos``, ``otrosConceptosRetributivos`` y asigno a ``salarioBruto``

Sumar ``IRP``,``Seguirdad Social`` y lo asigno a deducciones

``salarioNeto`` asigna ``salarioBruto`` -``deducciones``

Salida:

Escribir(``salarioBruto``,``salarioNeto``)

**Paso 3:** Escribir el pseudocódigo

```
Algoritmo Salario
# Entrada
	salarioBase<-Leer()
	pagasExtras<-Leer()
	complementos<-Leer()
	otrosConceptosRetributivos<-Leer()
	IRP<-Leer()
	seguridadSocial<-Leer()
# Proceso
salarioBruto<-salarioBase+pagasExtras+complementos+otrosConceptosRetributivos
deducciones<-IRP+seguridadSocial
# Salida
Escribir(salarioBruto,salarioNeto)
Fin Algoritmo
```



### Ejercicio 3

*Determinar la ruta para llegar a una ciudad por avión*

**Paso 1:** Definir el problema

Necesitamos la ruta de vuelo de un origen a un destino 

Para volar a otra ciudad, deberá encontrar el aeropuerto más cercano, llegar al aeropuerto más cercano, encontrar el aeropuerto más cercano a su destino, llevar el avión a ese aeropuerto y llegar desde el aeropuerto de destino a la ciudad

**Paso 2:** Poner la entrada, el proceso y la salida

Entrada

``Origen`` introducido por usuario

``Destino`` introducido por usuario

Proceso

Avisamos al usuario si introduce el mismo origen y destino

Calcular ruta de vuelo

Salida

Escribir Posible Ruta



**Paso 3:** Escribir el pseudocódigo

```
Algoritmo Vuelo
# Entrada
Origen<-Leer()
Destino<-Leer()
# Proceso
if Origen = Destino
	Escribir "Ya está aquí"
Else
	Mostrar <-(La ruta más corta y disponible entre Origen y Destino)
# Salida
Escribir(Mostrar)
Fin Algoritmo
```



### Ejercicio 4

*Calcula el área y perímetro de un círculo dado su radio*

**Paso 1:** Definir el problema

Tenemos que calcular el Área y Perímetro de un círculo, para ello hemos encontrado estas fórmulas

r=Radio

d= 2 * r

PI = 3.14

A= PI * r^2

Área del Círculo

P= PI * (2 * r)

Perímetro del Círculo

**Paso 2:** Poner la entrada, el proceso y la salida

Entrada:

``Radio``, ``PI``, ``Area``, ``Perímetro``

Proceso:

Asignamos a ``Radio`` un valor leído o entrado ``Radio`` <-()

Dar el valor a ``PI`` <-3.14 #Estático

Calcular el ``Area`` <-(``PI`` * ``Radio``^2)

Calcular el ``Perimetro`` <-(``PI`` * (2 * ``Radio``))

Salida:

Escribir resultado

**Paso 3:** Escribir el pseudocódigo

```
Algoritmo Circulo
# Entrada
Radio<-Leer()
PI<-"3.14"
If Radio <= 0 #Aseguramos que el valor introducido sea positivo
	Invalid Data
Else
# Proceso
Area<-(PI x Radio^2)
Perimetro<-(PI x (2 x Radio))
# Salida
Escribir(Area)
Escribir(Perimetro)
Fin Algoritmo
```



### Ejercicio 5

*Dada una lista de números enteros, determina cuál es el mayor y cuál es el menor*

**Paso 1:** Definir el problema

¿Cómo se sabe cuándo es mayor o menor?

Los símbolos de desigualdad más conocidos son: «mayor que» > y «menor que» < Con ellos podemos hacer comparaciones. **La apertura grande siempre señala al elemento más grande, y la terminación más pequeña, la punta, al más pequeño**.

Usuario Introduce lista de números (indeterminado)

Se comparan todos los números para saber:

Cual es el número ``Mayor``

Cual es el número ``Menor``

Debemos dar al usuario la posibilidad de incluir cuantos números quiera

**Paso 2:** Poner la entrada, el proceso y la salida

Entrada

``Mayor`` ``Menor`` 

Proceso

Usuario introduce la lista de números, almacenamos los valores con un bucle

Se comparan los números con el uso de un bucle

Se añade el valor más alto a ``Mayor`` y el valor más bajo a ``Menor``

Salida

Se escribe en la pantalla ``Mayor`` y ``Menor``

**Paso 3:** Escribir el pseudocódigo

```
Algoritmo MayorMenor
# Entrada
numerosAProcesar<-0
Mayor<-0
Menor<-0
# Proceso

numerosAProcesar<-input("¿Cuántos números quiere procesar?")

input_list
i <- 0
repeat
	user_input <- input()
		if user_input is not blank
			input_list[i] <- user_input
			i <- i+1
		endif
until user_input is blank

#Se comparan los numeros de la lista el mayor va a mayor y el menor va a menor
Menor <- input_list[0]
Mayor <- input_list[0]
i <-0

repeat
	if input_list[i] > Mayor
		Mayor <- input_list[i]
	end if 
	if input_list[i] < Menor
		Menor <- input_list[i]
	end if
	i <- i+1

# while i is less than the size of the list
 until i is great than numerosAProcesar

# Salida
Escribir(Mayor)
Escribir(Menor)
Fin Algoritmo
```



### Ejercicio 6

*Crea un algoritmo que convierta grados Celsius a Fahrenheit*

**Paso 1:** Definir el problema

Para convertir Fahrenheit a Celsius usamos la siguiente formula

``Fahrenheit`` = (``Celcius `` * 1.8) + 32

**Paso 2:** Poner la entrada, el proceso y la salida

Entrada

 ``Celcius ``se le asigna el valor entrado por el usuario

Proceso

Calcular ``Fahrenheit``

Salida

Escribir por la pantalla ``Fahrenheit``

**Paso 3:** Escribir el pseudocódigo

```
Algoritmo Fahrenheit
# Entrada
Celcius<-Leer()
# Proceso
Fahrenheit<-((Celcius x "1.8") + 32)
# Salida
Escribir(Fahrenheit)
Fin Algoritmo
```



### Ejercicio 7

*Dado un número entero, crea un algoritmo que determine si es par o impar.*

**Paso 1:** Definir el problema

Del ``numero`` introducido averiguar si es par o impar

**Un número es par si es múltiplo de dos**

**Un número impar es un número que no es divisible por 2, es decir no es múltiplo de 2** (Entiendo que el resto sería 1)

**Paso 2:** Poner la entrada, el proceso y la salida

Entrada

``numero`` se le asigna el valor entrado por el usuario

Proceso

Se calcula el resto de dividirlo entre 2

Salida

Si ``resultado`` es 0 escribimos par, si ``resultado`` es 1 escribimos impar, otro resultado posible lo marcamos como Error

**Paso 3:** Escribir el pseudocódigo

```
Algoritmo ParImpar
# Entrada
numero<-Leer()
# Proceso
resultado<- numero mod 2
# Salida
If resultado=0
	Escribir "Es par"
Else
	If resultado=1
		Escribir "Es Impar"
	Else
		Escribir "Error"
Fin Algoritmo
```

### Ejercicio 8

*Crea un algoritmo que determine si un año es bisiesto o no.*

**Paso 1:** Definir el problema

**Cualquier año divisible por 4 es un año bisiesto**: por ejemplo, 1988, 1992 y 1996 son años bisiestos

**Paso 2:** Poner la entrada, el proceso y la salida

Entrada

El usuario introduce el año

Proceso

Calculamos si es ``Bisiesto`` con el resto de dividirlo entre 4

Salida

Si el resto es 0 es bisiesto de lo contrario no lo es

**Paso 3:** Escribir el pseudocódigo

```
Algoritmo Bisiesto
# Entrada
Year<-Leer()
# Proceso
Bisiesto<-(year mod 4)
# Salida
if Bisiesto = 0
	Escribir "Es bisiesto"
else
	Escribir "No es bisiesto"
Fin Algoritmo
```

### Ejercicio 9

*Crea un algoritmo que determine si una cadena de texto es un palíndromo o no*

**Paso 1:** Definir el problema

Un palíndromo es una **palabra, frase, número, u otra secuencia de caracteres que se lee de la misma forma hacia adelante que hacia atrás**.

Debemos leerlo del revés y ver si es igual a la cadena introducida

**Paso 2:** Poner la entrada, el proceso y la salida

Entrada

Se le asigna el valor entrado por el usuario a ``stringUser``

Proceso

Invertimos la cadena ``stringUser`` y la añadimos a la variable ``stringUserInversed``

Salida

Si la cadena del usuario es igual a la cadena invertida es palíndromo, de lo contrario no lo será

**Paso 3:** Escribir el pseudocódigo

```
Algoritmo Palindromo
# Entrada
stringUser<-Leer()
# Proceso
stringUserInversed<-(stringUser lectura inversa)
# Salida
if stringUser = stringUserInversed
	Escribir "Es palíndromo"
Else
	Escribir "No es palíndromo"
Fin Algoritmo

#Ejercicio 9 hecho en clase
Algoritmo Palindromo
   # Entrada
   cadena <- leer()
   #Proceso
   #cadena <- Convertir a minúsculas y eliminar espacios en blanco
   reversa <- depuracionCadena(cadena)
   Si cadena es igual a reversa entonces
     resultado <- "La cadena es un palíndromo"
   Sino
     resultado <- "La cadena no es un palíndromo"
   Fin Si
   # Salida
   escribir resultado
Fin Algoritmo

SubAlgoritmo depuracionCadena (cadena)
    #quita los espacios en blanco, otros caracteres y convierte todo a minusculas
    i<-0
    Mientras cadena[i] sea diferente de findecadena Haga
        caracter<-""
        Si  el ASCII de cadena[i]  mayor que 64 y ASCII de cadena[i] menor que 91 Entonces
            caracter<-cadena[i] en minusculas
        Fin Si
        Si  el ASCII de cadena[i]  mayor que 96 y ASCII de cadena[i] menor que 123 Entonces
            caracter<-cadena[i]
        End Si
        temporal <- temporal + caracter
        Si caracter es diferente "" Entonces
            i<-i+1
        Fin Si
    Fin Mientras
    L<-i
    reversa<-""
    Para N = 0 Hasta L-1 Con Paso 1 Haga
        reversa    <-reversa+ temporal[i-1]
        i<-i-1
    Fin Para
    devuelva reversa
Fin SubAlgoritmo
```

### Ejercicio 10

*Dada una lista de nombres, crea un algoritmo que ordene la lista alfabéticamente*

**Paso 1:** Definir el problema

Ante una lista de palabras hay que ordenarlas alfabéticamente

Debemos seleccionar la primera letra de cada palabra y ordenarlas según el alfabeto

**Paso 2:** Poner la entrada, el proceso y la salida

Entrada

Usuario asigna números, que almacenamos en un bucle para generar la lista ``input_list``

Proceso

Asignamos a ``input_listOrdered`` el valor resultante de ordenarAlfabeticamente(input_list)

Salida

La lista ordenada

**Paso 3:** Escribir el pseudocódigo

```
Algoritmo Alfabetico
# Entrada
input_list
i <- 0
repeat
	user_input <- input()
	if user_input is not blank
		input_list[i] <- user_input
		i <- i+1
	endif
until user_input is blank
# Proceso
input_listOrdered <-ordenarAlfabeticamente(input_list)
# Salida
Escribir(input_listOrdered)
Fin Algoritmo
```

### Ejercicio 11

*Crea un algoritmo que calcule el factorial de un número entero*

**Paso 1:** Definir el problema

Factorial de un número es **el producto de los “n” factores consecutivos desde “n” hasta 1**. El factorial de un número se denota por n!

3 factorial is 6
6=3 * 2 * 1
7 factorial is 5040
5040 = 7 * 6 * 5 * 4 * 3 * 2 * 1

**Paso 2:** Poner la entrada, el proceso y la salida

Entrada

Usuario introduce ``numero``

Creamos la variable ``contador`` a 0

Creamos la variable ``factorial`` a 1

Proceso

Sumar ``contador`` de 1 en 1 hasta alcanzar el mismo valor que ``numero``

Cada vez que se ha incrementado ``contador`` lo multiplicamos por ``factorial`` y este resultado lo asignamos a ``factorial``

Salida

Escribir ``factorial``

**Paso 3:** Escribir el pseudocódigo

```
Algoritmo Factorial
# Entrada
numero<-Leer()
contador<-0
factorial<-1
# Proceso
Repetir
	contador <-contador+1
	factorial <-factorial multiplicado por contador
Hasta que contador igual a numero
# Salida
Escribir(factorial)
Fin Algoritmo
```

### Ejercicio 12

*Dado un número entero, crea un algoritmo que determine si es primo o no*

**Paso 1:** Definir el problema

Los números primos solo pueden ser divididos por ellos mismos y por 1

1 no es primo

Si alguno de los restos de esas divisiones es 0, el numero no será primo

El usuario introducirá un número y nuestro algoritmo debe indicarle si es primo o no

**Paso 2:** Poner la entrada, el proceso y la salida

Entrada

Asignamos a ``numero`` el valor que el usuario introduce por el teclado

Proceso

Para averiguar si es primo o no:

Introducir el numero por el teclado

Validar que sean números, si no lo son muestra error

Se define variable resultado

Para i=numero-1, mientras que sea mayor que 1, dividimos el numero entre 1

Hacemos un bucle desde el numero anterior hasta 1, dentro del bucle dividimos numero entre la variable del bucle y el resto lo almacenamos en resultado, si el resultado es 0, no es primo

Se imprime primo o no primo dependiendo el valor de las operaciones

Salida

Escribir si es primo o no

**Paso 3:** Escribir el pseudocódigo

```
Algoritmo NumeroPrimo
# Entrada
numero<-Leer()
resultado<-0
primo<-true
# Proceso
if numero = 1
			primo false
endif

si numero diferente a entero
	Escribir Error
sino
	para i=numero-1 hasta 2 con paso -1 hacer
    #version positiva del para para i=2 hasta numero-1 con paso +1 hacer

	#it then uses a loop, the loop value (i) starts at 34 (35 - 1) and goes down by one each loop until it 		#reaches 2
		

		
		resultado <- numero mod i
		#for each loop cycle, it checks if the number is divisible by the loop value (i)
		
		si resultado = 0
		#if it is, then the number is not prime and the loop terminates
		
			primo <- false
			i <- 2 #break, this would need to be changed for the positive version
		finsi
		
		#if it is not then the loop value (i) reaches 2 and the number is prime
	finpara
finsi

# Salida
si primo = false entonces
	Escribir "El numero no es primo"
sino entonces
	Escribir "El numero es primo"
Fin Algoritmo
```

so basically what this algorithm does it it takes a number, lets pick 35
it then uses a loop, the loop value (i) starts at 34 (35 - 1) and goes down by one each loop until it reaches 2
for each loop cycle, it checks if the number is divisible by the loop value (i)
if it is, then the number is not prime and the loop terminates
if it is not then the loop value (i) reaches 2 and the number is prime

### Ejercicio 13

*Crea un algoritmo que calcule el área y volumen de un cubo dado su lado*

**Paso 1:** Definir el problema

``Area`` <- 6 * ``lado``^2

``Volumen`` <-``lado``^3

**Paso 2:** Poner la entrada, el proceso y la salida

Entrada

Usuario introduce el lado

Proceso

Calculamos ``Area`` y ``Volumen``

Salida

Escribimos ``Area`` y ``Volumen``

**Paso 3:** Escribir el pseudocódigo

```
Algoritmo Cubo
# Entrada
lado<-Leer()
# Proceso
 #Area <- 6 x lado^2
	Area<- 6 multiplicado por (lado multiplicado por lado )
#Volumen <-lado^3
	Volumen<- (lado multiplicado por lado multiplicado por lado)
# Salida
Escribir(Area)
Escribir(Volumen)
Fin Algoritmo
```

### Ejercicio 14

*Dada una lista de números enteros, crea un algoritmo que calcule la suma de todos los números pares de la lista*

**Paso 1:** Definir el problema

Tenemos que calcular cuales son los numero que son pares y dichos pares sumarlos y mostrar el total

**Paso 2:** Poner la entrada, el proceso y la salida

Entrada

Asignamos a ``input_list``  ,con un bucle, los valores que el usuario introduce por el teclado

Proceso

Calculamos el resto al dividirlo entre 2 con cada numero y lo añadimos a una nueva lista `Par`

Solo sumamos los números cuyo resto haya sido 0 indicando ser par, sumando todos los valores que contiene `Par` y asignándolo a ``parResul``

Salida

Escribimos el resultado por la pantalla

**Paso 3:** Escribir el pseudocódigo

```
Algoritmo SumaPar
# Entrada
input_list
i <- 0
repeat
	user_input <- input()
	if user_input is not blank
		input_list[i] <- user_input
		i <- i+1
	endif
while user_input is not blank
# Proceso


i <-0 #Indica las posiciones de input_list
j <-0 #Indica las posiciones de par

repeat

	if input_list[i] mod 2 = 0 then
		Par[j] <- input_list[i]
		j <- j+1
		#Asigno a Par la lista con numeros pares
	endif
	i <- i+1

while i is less than the size of the list

j <-0

repeat
	parResul<-parResul + Par[j]
	j <- j+1
while i is less than the size of the list

# Salida
Escribir(parResul)

```

### Ejercicio 15

*Crea un algoritmo que determine si un número es positivo, negativo o cero*

**Paso 1:** Definir el problema

Debemos averiguar si un numero introducido es mayor, igual o menor que cero

**Paso 2:** Poner la entrada, el proceso y la salida

Entrada

Asignamos a ``numero`` el valor introducido por el usuario

Proceso y Salida

Si es mayor a 0 es positivo, si es menor a 0 es negativo si es igual a 0 es cero

**Paso 3:** Escribir el pseudocódigo

```
Algoritmo PositivoNegativoCero
# Entrada
numero<-Leer()
# Proceso
if numero > 0
	Escribir(Es positivo)
Else
	if numero < 0
		Escribir(Es negativo)
	Else
		if numero = 0
			Escribir(Es cero)
		Else
			Error
# Salida
Fin Algoritmo
```

### Ejercicio 16

*Dada una lista de números enteros, crea un algoritmo que calcule la media de la lista*

**Paso 1:** Definir el problema

Para hacer la media debemos sumar todos los números de la lista y dividirlo por la cantidad de números

**Paso 2:** Poner la entrada, el proceso y la salida

Entrada

``suma``

Usuario define la lista y sin que lo sepa ya se lo estaremos sumando y asignando a ``suma``

Proceso

Se calcula la ``media`` al dividir ``suma`` / ``i``

Salida

Se escribe ``media`` por la pantalla

**Paso 3:** Escribir el pseudocódigo

```
Algoritmo Media
# Entrada
suma<-0
Define input_list
i <- 0
repeat
	user_input <- input()
	if user_input is not blank
		input_list[i] <- user_input
		i <- i+1
		suma<-(suma + user_input)
	endif
while user_input is not blank
# Proceso
media<- (suma/i)
# Salida
Escribir(media)
Fin Algoritmo
```

### Ejercicio 17

*Crea un algoritmo que genere un número aleatorio entre 1 y 100, y le pida al usuario adivinarlo. El algoritmo deberá indicar si el número introducido es mayor o menor que el número aleatorio, hasta que el usuario adivine el número correcto*

**Paso 1:** Definir el problema

Debemos generar un numero aleatorio entre 1 y 100

Usuario tiene que adivinarlo

Cada vez que usuario falle se le indicará si el numero que introdujo es más grande o más pequeño

Si el usuario acierta se le felicita

**Paso 2:** Poner la entrada, el proceso y la salida

Entrada

Generamos un ``randomnumber`` entre 1 y 100

Proceso

Repetimos el que usuario defina ``usernumber`` hasta que sea igual que ``randomnumber``

Si ``usernumber`` es menor que ``randomnumber`` escribimos por la pantalla "es más pequeño"

Si ``usernumber`` es mayor que ``randomnumber`` escribimos por la pantalla "es más grande"

Salida

Escribir "Lo adivinaste"

**Paso 3:** Escribir el pseudocódigo

```
Algoritmo AdivinaNumero
# Entrada
randomnumber<-genRandomInt[1, 100]

# Proceso
Repetir
usernumber<-Leer()
	if usernumber < randomnumber
		Escribir "Tu numero es más pequeño"
	Else
		if usernumber > randomnumber
			Escribir "Tu numero es más grande"
		else
Hasta que usernumber = randomnumber
# Salida
Escribir "Lo adivinaste"
Fin Algoritmo
```

### Ejercicio 18

*Crea un algoritmo que determine si una cadena de texto es un anagrama de otra cadena de texto*

**Paso 1:** Definir el problema

¿Cómo se hace un anagrama?

Un anagrama es una palabra que resulta de la **transposición de todas las letras de otra palabra**. Dicho de otra forma, una palabra es anagrama de otra si las dos tienen las mismas letras, con el mismo número de apariciones, pero en un orden diferente.

Debemos asegurar que se usaron la misma cantidad de caracteres y del mismo tipo

**Paso 2:** Poner la entrada, el proceso y la salida

Entrada

Usuario añade valores a las variables ``String1`` ``String2``

Proceso

Calculamos que tengan el mismo número de caracteres

Si es así contamos cada tipo de letra

Salida

Si todo coincide escribimos por la pantalla que si de lo contrario no

**Paso 3:** Escribir el pseudocódigo

```
Algoritmo Anagrama
# Entrada
String1<-Leer()
String2<-Leer()
# Proceso
Lenght1<-contarElementosLista(String1)
Lenght2<-contarElementosLista(String2)
If Lenght1 es igual a Lenght2
	i <- 0
	resultado <-"es anagrama"
	Mientras i sea menor o igual que Lenght1-1
		noEstaLetra <-True
		Para j=i Hasta Lenght1-1 con paso 1 Hacer
			If String1[i] es igual a String2[j] then
				posicion <-j
				noEstaLetra <- False
			Endif
		FinPara
		If noEstaLetra es igual a True then
			resultado <- "no es un anagrama"
			i <- n
		Else
			temp <- String2[i]
			String2[i] <- String1[i]
			String2[position] <- temp
			i <- i+1
		Endif
	FinMientras
Endif

        #If Lenght1 es igual a Lenght2
            #For String1 count every type of letter and add it to String1value
            #For String2 count every type of letter and add it to String2value

                #If String1value = String2value
                    #Escribir "Es un anagrama"
                #Else
                    #Escribir "No es un anagrama"
        #Else
            #Escribir "No es un anagrama"
# Salida
Escribir(resultado)
Fin Algoritmo
```

### Ejercicio 19

*Dada una lista de números enteros, crea un algoritmo que elimine los números duplicados de la lista*

**Paso 1:** Definir el problema

Ningún número debe ser repetido

**Paso 2:** Poner la entrada, el proceso y la salida

Entrada

Asignamos a ``input_list``  ,con un bucle, los valores que el usuario introduce por el teclado

Proceso

Eliminamos duplicados

Salida

Lista sin duplicados

**Paso 3:** Escribir el pseudocódigo

```
Algoritmo DuplicadosFuera
# Entrada
input_list = list([2, 5, 7, 9, 7, 73, 4, 2, 5, 8]);
i = 0;
# Proceso

while (i < len(input_list)):
    j = i+1;
    while (j < len(input_list)):
        if input_list[i] == input_list[j]:
            del input_list[j]
        else:
            j = j + 1;
    i = i + 1;

# Salida
print(input_list)

Fin Algoritmo
```

### Ejercicio 20

*Crea un algoritmo que determine si un número es capicúa o no*

**Paso 1:** Definir el problema

**Aquellos que se leen igual de izquierda a derecha y de derecha a izquierda**. Pongamos un ejemplo. El 23032 sería capicúa.

**Paso 2:** Poner la entrada, el proceso y la salida

Entrada

 ``numero``

Proceso

Se invierte ``numero`` y se añade a ``numeroAlReves``

Si ``numero``=``numeroAlReves`` asignar a ``resultado`` "es capicúa" de lo contrario  asignar "no es capicúa"

Salida

Escribir `resultado`

**Paso 3:** Escribir el pseudocódigo

```
Algoritmo Capicua
# Entrada
numero<-Leer()
# Proceso
numeroAlReves<-(numero lectura inversa)
If numero = numeroAlReves
	Resultado <- "Es capicúa"
Else
	Resultado <- "No es capicúa"
# Salida
	Escribir(Resultado)
Fin Algoritmo
```

