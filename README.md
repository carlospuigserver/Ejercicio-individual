# Ejercicio individual, 5 ejercicios en pseudocódigo


La dirección GitHub de este repositorio es la siguiente: https://github.com/carlospuigserver/Ejercicio-individual.git


### Ejercicio 08

***Algoritmo impuestos:***
* Calcular precio producto añadiendo IVA

***Entrada:***
* coste producto: REAL
* IVA: coste producto + [coste producto*(0,21)]

***Precondición***: coste producto > 0

***Variables***:
* Coste inicial ( precio de un producto culquiera sin aplicarle ningún impuesto)
* Coste final ( precio de un producto cualquiera habiéndole aplicado el impuesto IVA)
***Realización***
```
Calcular precio producto:
Coste inicial = coste cualquier producto sin IVA= x
Aplicación IVA= (x*0,21)
Coste final= x + (x*0,21)
```
***fin Algoritmo impuestos***




### Ejercicio 09

***Algoritmo 1:***
* Realización media ponderada de unos ciertos números y de sus respectivos coeficientes de ponderación

***Entrada:***
* Número 01: REAL
* Número 02: REAL
* Número 03: REAL
* Coef Ponderación 01: REAL
* Coef Ponderación 02: REAL
* Coef Ponderación 03: REAL


***Variables***
* Resultado media aritmética final
* Resultado media ponderada final


***Realización:***
```
Resultado media aritmética final= (Número 01 + Numero 02 + Número 03)/ 3
Resultado media ponderada final
```

***fin Algoritmo 1***



### Ejercicio 10

***Algoritmo 1:***
* Cálculo del área de un triángulo a partir de un lado y su altura

***Entrada:***
* Lado 1: REAL ( base del triángulo)
* ALTURA:REAL

***Variables***
* Resultado área triángulo

***Precondición***
* Lado 1 > 0
* Altura > 0

***Realización:***
```
Resultado área triángulo = [ (Lado 1) * (Altura)] / 2
```

***fin Algoritmo área***


***Algoritmo 2:***
* Cálculo del área de un triángulo a partir de sus dos lados perpendiculares


***Entrada:***
* Lado 1: REAL ( cateto 1)
* Lado 2: REAL ( cateto 2)

***Variables***
* Resultado área triángulo

***Precondición***
* Lado 1 > 0
* Lado 2 > 0

***Realización:***
```
Resultado área triángulo = [ (Lado 1) * (Lado 2)] / 2
```
***fin Algoritmo 2***

***Se puede realizar***




### Ejercicio 11

***Algoritmo 1:***
* Remuneración de horas extra – Solución de principio

***Algoritmo horas_extra:***
* Establece la remuneración de `horas_ext' adicionales para
* un salario mensual bruto de `salario_mensual_bruto'.

***Entrada***
* salario_mensual_bruto : REAL
* Importe del salario mensual bruto
* horas_ext : ENTERO
* Cantidad de horas extra del mes a pagar





