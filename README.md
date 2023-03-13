# RETO 5 
Se resolveran los problemas planteador por medio de un notebook de python, y los codigos que se hicieron seran subidos a este repositorio.

### Recurso
[![68747470733a2f2f692e706f7374696d672e63632f3768483173474a312f696d6167652e706e67.png](https://i.postimg.cc/SKJQPXK1/68747470733a2f2f692e706f7374696d672e63632f3768483173474a312f696d6167652e706e67.png)](https://postimg.cc/061qMyD7)

### Dado un número entero, determinar si ese número corresponde al código ASCII de una vocal minúscula.


```
n:int
n = int(input("Ingrese un numero: "))
if n == 97 or n == 101 or n == 105 or n == 111 or n == 117 :
    print("El número corresponde al codigo ASCII de una vocal minuscula la cual es: " + str(chr(n)))
else:
    print("El número NO corresponde al codigo ASCII de una vocal minuscula")
```
Para este primer codigo se tiene en cuenta la tabla de caracteres ASCII en donde se puede evidenciar que para las vocales en minuscula les corresponde los siguientes numeros enteros:
97 -> a
101 -> e
105 -> i
111 -> o
117 -> u
al digitar alguno de esos numeros saldra que es una vocal minuscula en codigo ASCII, de lo contrario saldra que no lo es



### Dada una cadena de longitud 1, determine si el código ASCII de primera letra de la cadena es par o no.
```
cadena=input("introduce una cadena de longitud 1: ")
if ord(cadena) % 2 == 0:
    print("EL código ASCII de la primera letra de la cadena es par")
else:
    print("EL código ASCII de la primera letra de la cadena NO es par")
```
En este punto  se usa tambien la tabla de caracteres del codigo ASCII en donde al digitar  caracteres como:
a -> 97
b -> 98
A los numeros que se obtienen se les sacara el modulo entre 2, si el modulo es cero, significara que el numero es par, en este caso "a" corresponde a un codigo ASCII impar, mientras que la "b" corresponde a un codigo ASCII par.

### Dado un carácter, construya un programa en Python para determinar si el carácter es un dígito o no. 
```
n=input("introduce un caracter: ")
if 48<= ord(n) <=57:
     print("EL carácter es un digito")
else:
    print("EL carácter NO es un digito")
```
En este codigo al digitar se evidenciara si los caracteres que se digitan pertenencen a los codigos ASCII entre  48 y 57, si es asi se imprimira que "EL carácter es un digito" debido a que esos codigos pertenecen de los numeros del 0 al 9, de lo contrario se imprimira "EL carácter NO es un digito".
### Dado un número real x, construya un programa que permita determinar si el número es positivo, negativo o cero. Para cada caso de debe imprimir el texto que se especifica a continuación:
```
n:float
n=float(input("introduce un numero: "))
if n > 0:
    print("El número " +str(n)+ " es positivo")
elif n < 0:
    print("El número "  +str(n)+ " es negativo")
else:
    print("el número " +str(n)+ " es el neutro para la suma")
```
En este codigo se tomara a los numeros mayores de cero como positivos, a los menos de cero como negativos, y al cero como el numero netro para la suma.
## Dado el centro y el radio de un círculo, determinar si un punto de R2 pertenece o no al interior del círculo.
```
centro_x=float(input("el punto en x del centro del circulo"))
centro_y=float(input("el punto en y del centro del circulo "))
radio=float(input("El radio del circulo"))
punto_x=float(input("ingresar un punto x"))
punto_y=float(input("ingresar un punto y"))
if ((punto_x - centro_x)**2 + (punto_y - centro_y)**2 )**0.5 <= radio:
    print("los puntos (" +str(punto_x) + "," +str(punto_y) + ") estan dentro del circulo con radio " +str(radio) + " y con centro (" +str(centro_x) + "," +str(centro_y) + ")" )
else:
    print("los puntos (" +str(punto_x) + "," +str(punto_y) + ") no estan dentro del circulo con radio " +str(radio) + " y con centro (" +str(centro_x) + "," +str(centro_y) + ")" )
```
Para este codigo se uso la ecuacion:
$$\sqrt{(x-h)^2 + (y- k)^2)} <= r$$ 
Tomando como (x,y) como la coordenada que se quieren saber si esta dentro de la circuferencia, a (h,k) como las coordenadas del centro de la circuferencia y a "r" como radio de la circuferencia, en esta operacion si se cumple la condicion, se imprime que (x,y) si se encuentran dentro del circulo, de lo cont contrario se imprime que (x,y) no estan dentro del circulo.



## Dadas tres longitudes positivas, determinar si con esas longitudes se puede construir un triángulo.
```
a=float(input("Inserte una longitud 'a' para el triangulo"))
b=float(input("Inserte una longitud 'b' para el triangulo"))
c=float(input("Inserte una longitud 'c' para el triangulo"))
if abs(b-c) < a <(b+c) or abs(a-c) < b < (a+c) or abs(a-b) < c < (a+b):
    print("Es un triangulo")
else:
    print("No es un triangulo")
 ```
    
Para este codigo se usa la operacion en donde, si el lado mayor del triangulo se encuentra entre el valor absoluto de la resta de los otros dos lados y la suma de los otros dos lados, se considera que estos tres lados pueden formar un triangulo es decir:
$$|a-b|< c < (a+b)$$
tomando a "c" como el lado mayor del triangulo, y  "a" y  "b" como los lados menores.
Para el codigo se busco la función "abs(x)" de python en donde saca el valor absoluto de la operación, para asi evitar problemas en donde se aceptan lados negativos o de valor cero como posibles de un triangulo. 

Pero al ser una función de python no vista se realizo otro codigo nuevamente, en donde se añaden mas condicionales para evitar el problema mencionado anteriormente 
   ```   
   a=float(input("Inserte una longitud 'a' para el triangulo"))
b=float(input("Inserte una longitud 'b' para el triangulo"))
c=float(input("Inserte una longitud 'c' para el triangulo"))
if b>c and (b-c) < a <(b+c) :
    print("Es un triangulo")
elif b<c and  (c-b) < a <(b+c) :
    print("Es un triangulo")
elif a>c and (a-c) < b < (a+c):
    print("Es un triangulo")
elif a<c and (c-a) < b < (a+c):
    print("Es un triangulo")
elif a>b and (a-b) < c < (a+b):
    print("Es un triangulo")
elif a>b and (a-b) < c < (a+b):
    print("Es un triangulo")
elif a ==b and a ==c:
    print("Es un triangulo")
else:
    print("No es un triangulo")
  ```
  
  Muchas gracias por leer :D.