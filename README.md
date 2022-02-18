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


***precondición***
* salario_mensual_bruto > 0
* horas_ext ≥ 0


***constante***

CANTIDAD_SEMANAS : ENTERO ← 52
*Cantidad de semanas de trabajo

CANTIDAD_HORAS_SEMANA : ENTERO ← 35
* Cantidad legal de horas de trabajo semanales
    
CANTIDAD_HORAS_MAX_1 : ENTERO ← 8
* Umbral de cambio de precio de remuneración
    
PRECIO_1 : REAL ← 1,25
* Tarifa de remuneración de CANTIDAD_HORAS_MAX_1 primeras
* horas extra
   
PRECIO_2 : REAL ← 1,50
* Tarifa de remuneración de las otras horas extra


***variable***

horas_ext_1 : ENTERO
* Cantidad de horas extra con PRECIO_1 %
    
horas_ext_2 : ENTERO
* Cantidad de horas extra con PRECIO_2 %
    
precio_hora : REAL
* Precio hora de la remuneración bruta de base




***realización:***
``` 
Cálculo del precio_hora de la remuneración bruta de base
precio_hora ← precio_hora_bruto(salario_mensual_bruto)

Cálculo de la cantidad de horas de cada categoría
horas_ext_1 ← inf(horas_ext, CANTIDAD_HORAS_MAX_1)
horas_ext_2 ← sup(horas_ext – CANTIDAD_HORAS_MAX_1, 0)

Cálculo de la remuneración de las horas extra
Resultado ← precio_hora x (horas_ext_1 x PRECIO_1 + horas_ext_2 x PRECIO_2)
```



***fin horas_extra***
