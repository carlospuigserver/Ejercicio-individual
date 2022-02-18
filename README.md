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







### Ejercicio 12

***tipo CUENTA estructura***
* Versión simplificada
* saldo : REAL
* invariante
* El descubierto no está autorizado
* saldo ≥ 0

***fin CUENTA***



***Algoritmo 1:*** 
* Definición de abrir una cuenta



***abrir***
(c : CUENTA ; saldo_inicial : REAL)
    * Inicializar `c' mediante un `saldo_inicial'.

***Precondición***
* saldo_inicial > 0

***realización***
* c.descubierto ← 0
* c.saldo ← saldo_inicial

***postcondición***
* c.descubierto = 0
* El descubierto no está autorizado

* antiguo(saldo_inicial) = saldo_inicial
* c.saldo = saldo_inicial

***fin abrir***



***postcondición***
   
* c.saldo = antiguo(c).saldo + saldo_inicial




***Algoritmo 2:***

* abonar una cuenta

abonar(c : CUENTA ; crédito : REAL)
    * Crédito c de la suma crédito.

***Precondición***
   * c.saldo ≠ NULO
   * crédito ≠ NULO

***realización***
     *c.saldo ← c.saldo + crédito

***postcondición***
* El descubierto autorizado y el importe del crédito no se modifican
* antiguo(c).descubierto = descubierto
* antiguo(c).crédito = crédito

*  El saldo aumenta con el crédito
* c.saldo = antiguo(c).saldo + crédito

***fin abonar***



***Algoritmo 3:***
* cargar una cuenta

*cargar(c : CUENTA ; débito : REAL)
    * Carga `c' con la suma `débito'.

***Precondición***
    * c.saldo ≠ NULO
    * débito ≠ NULO
    * c.saldo + c.descubierto ≥ débito ≥ 0

***realización***
    abonar(c, –débito)

***postcondición***
    *  El descubierto autorizado y el importe del `débito' no se
    *  modifican
    * antiguo(c).descubierto = descubierto
    * antiguo(débito) = débito

    * Al saldo se le resta el `débito'
   * c.saldo = antiguo(c).saldo – débito

***fin cargar***


***Algoritmo 4:***  
* función consultar una cuenta

* consultar(c : CUENTA) : REAL
    *  El `saldo' de la cuenta `c'.

***precondición***
   * c.saldo ≠ NULO

***realización***
     * Resultado ← c.saldo

***postcondición***
   * Resultado = c.saldo

***fin consultar***



***Algoritmo 5:*** 
* Definición de es_acreedora


* es_acreedora(c : CUENTA) : BOOLEANO
    * ¿c es acreedora?

***precondición***
    * c.saldo ≠ NULO

***Realización***
    * Resultado ← (c.saldo > 0)

***postcondición***
    * Resultado = (c.saldo > 0)

***fin es_acreedora***



***Algoritmo 5:***
* Definición de es_deudora


* es_deudora (c : CUENTA) : BOOLEANO
    * ¿c es deudora?

***precondición***
    * c.saldo ≠ NULO

***Realización***
    * Resultado ← (– c.descubierto ≤ c.saldo ≤ 0)

***postcondición***
    * Resultado = (– c.descubierto ≤ c.saldo ≤ 0)

***fin es_deudora***



***Algoritmo 6:*** 
* Definición de abrir una cuenta con descubierto autorizado
 
 
 * abrir(c : CUENTA ; saldo_inicial : REAL ; descubierto_MAX : REAL)
    * Inicializar c mediante un saldo_inicial y un descubierto_MAX.

***Precondición***
    * saldo_inicial > 0
    * descubierto_MAX ≥ 0

***realización***
    * c.descubierto ← descubierto_MAX
    * c.saldo ← saldo_inicial

***postcondición***
    * c.descubierto = descubierto_MAX
    * c.saldo = saldo_inicial

***fin abrir***



***tipo CUENTA estructura***
    * Cuenta con descubierto autorizado con una duración limitada.

    saldo : REAL
    descubierto : REAL      # importe del descubierto autorizado
    fecha_descubierto : FECHA # decha de inicio del último descubierto
    duración_max : FECHA      # Duración máxima del descubierto

    ***invariante***
        * El descubierto está autorizado durante un tiempo limitado:
        
        *descubierto ≥ 0
        *fecha_descubierto ≠ 0 => fecha_descubierto + duración_max ≤ fecha_actual

        * el saldo debe ser superior al descubierto autorizado  saldo ≥ descubierto


***fin CUENTA***



***Algoritmo 7:***
* Definición de abrir una cuenta con descubierto autorizado durante un tiempo limitado

Algoritmo abrir
    * Inicializar c mediante un saldo_inicial y un
    * descubierto_MAX durante una duración_max.

Entrada
    * c : CUENTA
    * saldo_inicial : REAL
    * descubierto_MAX : REAL
    * duración_max : FECHA

Precondición
    * saldo_inicial > 0
    * descubierto_MAX ≥ 0
    * duración_max ≥ 0

realización
    * c.descubierto ← descubierto_MAX
    * c.saldo ← saldo_inicial
    * c.fecha_descubierto ← 0
    * c.duración_max ← duración_max

postcondición
    * c.descubierto = descubierto_MAX
    * c.saldo = saldo_inicial
    * c.duración_max = duración_max
    * c.fecha_descubierto = 0

***fin abrir***

 
