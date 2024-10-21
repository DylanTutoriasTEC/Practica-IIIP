# 2024 Semestre 2 - Práctica Tercer Parcial

## Instrucciones Generales
- El archivo **debe** llamarse **Examen3.py**
- **Debe** respetar el nombre de las funciones y el nombre de los parámetros que más adelante se describen
- Deben contruir las funciones con **Python**
- Debe utilizar la programación solo por **recursión** 
- Debe crear los comentarios de cada función tomando en cuenta **Nombre**, **Entrada**, **Salida** y **Restricciones**
- Recordar que en este caso por evaluar vectores o matrices **no se debe recortar**, solo el recorrido es por sus índices
- Pueden hacer uso **Try/Except, isinstance, type**
- Pueden hacer el uso de las funciones que se va creando durante el examen
- En todos los problemas aquí expuestos debe de validarse:
	-  de que los vectores acepten solo números enteros
	-  la matriz no debe ser nula
	-  deben ser homogéneas y del mismo largo
	-  los mensajes de error deben ser claros
- Cada pregunta vale 10 puntos:
 	- 1 punto comentarios
 	- 2 puntos validaciones
 	- 7 puntos resolución del problema

## Suma de dígitos pares

Escriba una función recursiva llamada sumaDigitosPares(num) que reciba como entrada un número entero positivo y retorne la suma de los dígitos que sean números pares. Si el número es negativo o no tiene dígitos pares, la función debe retornar un mensaje de error o 0, respectivamente.

``` python
>>> sumaDigitosPares(123456)
12  # 2 + 4 + 6 = 12
>>> sumaDigitosPares(1357)
0   # No hay dígitos pares
>>> sumaDigitosPares(-42)
"Error, el número debe ser positivo"
```

## Número espejo

Escriba una función recursiva llamada esEspejo(num) que reciba un número entero positivo y determine si es un número espejo. Un número espejo es aquel que es igual al número formado por sus dígitos en orden inverso.

``` python
>>> esEspejo(121)
True  # 121 es igual al revés
>>> esEspejo(12321)
True  # 12321 es igual al revés
>>> esEspejo(123)
False # 123 no es igual al revés
```

## Número piramidal

Escriba una función recursiva llamada esPiramidal(num) que reciba un número entero positivo y determine si es un "Número Piramidal". Un número piramidal es aquel que puede escribirse como la suma de los primeros n números naturales consecutivos. Por ejemplo, 6 es piramidal porque 6 = 1 + 2 + 3.

``` python
>>> esPiramidal(6)
True  # 6 = 1 + 2 + 3
>>> esPiramidal(10)
False # No se puede formar como suma de números consecutivos
>>> esPiramidal(15)
True  # 15 = 1 + 2 + 3 + 4 + 5
```

## numeroHermano(num)

Escriba un programa con sintaxis Python cuya función principal se llame **numeroHermano(num)**, que reciba como entrada un **número entero positivo** denominado num y que retorne si cumple (True) o no los requisitos (False) de número hermano. Un número hermano es un número natural y que posee al menos dos divisores primos (el 1 no es primo):

Ejemplos del comportamiento de la función:

```python
>>>numeroHermano(20) #(divisores propios: 2, 4, 5, 10)
True
>>> numeroHermano(8) #(divisores propios: 2,4)
False
>>> numeroHermano(-8)
"Error en la entrada, debe ser número positivo"
```

## numero polimax

Escriba una función llamada esPolimax(num) que reciba como entrada un número entero positivo num y determine si es un "Número Polimax". Un número es Polimax si, al dividirlo en dos mitades de igual longitud, ambas mitades tienen la misma cantidad de dígitos pares e impares. Si el número tiene una cantidad par de dígitos, y las dos mitades tienen la misma cantidad de dígitos pares e impares, la función debe retornar True; de lo contrario, debe retornar False.

```python
>>> esPolimax(123321)
True  # Mitades: 123 y 321 (1 par, 2 impares en cada mitad)
>>> esPolimax(1221)
False # Mitades: 12 y 21 (1 par, 1 impar en la primera mitad; 0 pares, 2 impares en la segunda mitad)
>>> esPolimax(123456)
False # Mitades: 123 y 456 (0 pares, 3 impares en la primera mitad; 3 pares, 0 impares en la segunda mitad)
>>> esPolimax(4444)
True  # Mitades: 44 y 44 (2 pares, 0 impares en cada mitad)
>>> esPolimax(123)
False # Cantidad impar de dígitos
```

## sumasEnDiagonal(matriz)

Escriba un programa con sintaxis Python cuya función principal se llame sumasEnDiagonal(matriz), que reciba como entrada una matriz (lista de listas de enteros) de tamaño cuadrado impar. Esta función retornará la suma de los elementos de las dos diagonales principales de la matriz. No se debe contar dos veces el elemento central de la matriz.

### Restricciones:
- La matriz debe ser cuadrada (mismo número de filas y columnas).
- El tamaño de la matriz debe ser un número impar.

Ejemplos del comportamiento de la función:

```python
>>> sumasEnDiagonal([[2, 0, 3],
                     [4, 5, 6],
                     [7, 8, 9]])
31  # (2 + 5 + 9) + (3 + 5 + 7) - 5

>>> sumasEnDiagonal([[1, 0, 1],
                     [0, 1, 0],
                     [1, 0, 1]])
5   # (1 + 1 + 1) + (1 + 1 + 1) - 1
```

## esParLigado(lista)

Escriba un programa con sintaxis Python cuya función principal se llame esParLigado(lista), que reciba como entrada una lista de números enteros. Esta función retornará True si siempre que aparece un número par, este es seguido por un número impar, o False en caso contrario. En el caso de que la lista termine en un número par, se considerará que no está ligado a un impar, por lo que la función retornará False.

```python
>>> esParLigado([2, 3, 4, 7, 8, 9])
True
>>> esParLigado([2, 4, 6, 8])
False
>>> esParLigado([5, 7, 9])
True
>>> esParLigado([2, 3, 6, 8, 10])
False
```

## esVectorOrdenado(vector, forma)

Escriba un programa con sintaxis Python cuya función principal se llame **esVectorOrdenado(vector, forma)**, que reciba como entradas un **vector** y una **forma**, este último será un string que especificará si el vector está ordenado en forma **ascendente o descendente**. Esta función retornará **True** si el vector corresponde al tipo de ordenamiento o **False** del caso contrario. No se puede usar su representación inversa o reversa del número

Los valores para **forma** son:  'asc' o 'desc'

```python
>>> esVectorOrdenado([23, 656, 5533, 8120], 'asc')
True
>>> esVectorOrdenado([15, 4, 0], 'desc')
True
>>> esVectorOrdenado([11, 45], 'desc')
False
```

## digitoMayoryMenor(lista)

Escriba un programa con sintaxis Python cuya función principal se llame **digitoMayoryMenor(lista)**, que reciba como entrada una **lista** con número **enteros**, y que retorne una lista de nuevos números que estará compuesto por los dígitos mayor y menor del número analizado.

```python
>>> digitoMayoryMenor([2300, 6756])
[30, 75]
>>> digitoMayoryMenor([2300, 6756, -99, 1001, 91823])
[30, 75, -99, 10, 91]

```

## matriz_triangular_inversa(matriz)

Escriba un programa con sintaxis Python cuya función principal se llame matriz_triangular_inversa(matriz), que reciba como entrada una matriz (lista de listas de enteros) de tamaño n x n. La función retornará True si todos los elementos que están debajo de la diagonal inversa de la matriz son múltiplos de 3, o False en caso contrario.

### Restricciones:
- El tamaño de la matriz debe ser cuadrado (n x n) con n mayor o igual a 4.

```python
>>> matriz_triangular_inversa([[3, 2, 1, 4],
                               [9, 3, 2, 1],
                               [6, 12, 3, 2],
                               [15, 9, 6, 3]])
True

>>> matriz_triangular_inversa([[3, 2, 1, 4],
                               [9, 3, 2, 1],
                               [6, 12, 3, 2],
                               [15, 8, 6, 3]])
False
```

## comprimirMatriz(matriz)
	
Escriba una solución con sintaxis Python cuya función principal se llame **comprimirMatriz(matriz)**, recibe como parámetro de entrada una matriz **válida** y lo que se debe realizar es retornar una matriz donde sus vectores o filas son el resultado de la suma de su vector adyacente, en el caso de que la matriz tenga filas impar, la última no será sumada:

matriz = [[2, 15], [8, 12], [5, 6], [30, 50]]

resultado = [[28, 27], [35, 56]]

![image](https://user-images.githubusercontent.com/1167750/167149485-583e0ab8-8991-4996-84c6-7af407327b24.png)


```python
>>> comprimirMatriz([[20, 15], [8, 12], [5, 6], [30, 50]])
[[28, 27], [35, 56]]

>>> comprimirMatriz([[2, 15, 2], [8, 12, 10], [5, 6, 0], [30, 50, 15], [5, 8, 6], [10, 12, 100]])
[[10, 27, 12], [35, 56, 15], [15, 20, 106]]

```

