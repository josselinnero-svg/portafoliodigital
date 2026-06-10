## Unidad2

<details>
<summary><b>🔮 Estructuras Condicionales (Selectivas)</b></summary>
<blockquote>
Estas estructuras permiten tomar decisiones dentro de un programa evaluando una expresión lógica
  
  ♦️ Tipos de estructuras selectivas  
  
* Simple: Evalúa una condición. Si es verdadera, ejecuta una instrucción; si es falsa, no hace nada
Diagrama de flujo: Se representa con un rombo para la condición. Si es "Verdadera", baja a la instrucción; si es "Falsa", salta directamente al final.
  
<img width="483" height="393" alt="image" src="https://github.com/user-attachments/assets/691cacba-af7e-412f-ad43-998084a9af8a" />
  
Pseudocódigo: Si condición entonces Realizar instrucciones Fin si

* Doble: Permite elegir entre dos alternativas. Si la condición es verdadera, ejecuta una acción; si es falsa, ejecuta otra.
Diagrama de flujo: El rombo de condición tiene dos caminos: uno para "Verdadera" y otro para "Falsa", cada uno con su bloque de instrucciones.

<img width="733" height="393" alt="image" src="https://github.com/user-attachments/assets/1069e197-5f13-4115-842d-8ed487a2cc8c" />

Pseudocódigo: Si condición entonces Realizar instrucciones 1 Si no Realizar instrucciones 2 Fin si

* Múltiple: Evalúa varias condiciones en cascada (varios "si" anidados) hasta encontrar la correcta.
Diagrama de flujo: Un punto de decisión del cual parten múltiples flechas hacia diferentes instrucciones

<img width="551" height="991" alt="image" src="https://github.com/user-attachments/assets/ff8d6fcf-1cf5-4f44-9e36-56626ec2cd48" />

Pseudocódigo: Consiste en una serie de estructuras Si... entonces... sino una dentro de otra

</blockquote>
</details>
  
<details>
<summary><b>🔮 Estructuras Repetitivas (Iterativas o Bucles) (Selectivas)</b></summary>
<blockquote>  
Permiten repetir un conjunto de instrucciones un número determinado de veces o mientras se cumpla una condición

  
  🍄 Tipos de estructuras selectivas

* Mientras (While): El bucle se repite mientras la condición sea verdadera. Si la condición es falsa desde el inicio, las instrucciones nunca se ejecutan
  
Diagrama de flujo: El rombo de condición está al inicio del bucle. Si es verdadera, ejecuta la instrucción y vuelve a la condición

<img width="407" height="388" alt="image" src="https://github.com/user-attachments/assets/6c15a317-95ec-4bea-8c0a-643845a88bae" />


Pseudocódigo: Mientras condición hacer Realizar instrucciones Fin Mientras

* Hacer Mientras (Do-While): Similar al "mientras", pero las instrucciones se ejecutan al menos una vez, ya que la condición se evalúa al final

Diagrama de flujo: El bloque de instrucciones va primero, seguido por el rombo de condición

<img width="342" height="356" alt="image" src="https://github.com/user-attachments/assets/e87aa1f9-2fcc-4af2-acd7-f7914f3cf0c7" />

Pseudocódigo: Hacer Realizar instrucciones Mientras condición Fin Mientras

* Desde/Para (For): Se utiliza cuando se conoce de antemano el número de iteraciones. Utiliza una variable índice, un valor inicial y un valor final
Diagrama de flujo: Incluye la inicialización del índice, la comparación con el valor final, la ejecución de instrucciones y el incremento automático del índice.

<img width="475" height="367" alt="image" src="https://github.com/user-attachments/assets/24eceabf-396f-4d5a-9a7b-56f74683262b" />

Pseudocódigo: para vo asignar vi hasta vf incrementar hacer realizar instrucciones fin para
  
</blockquote>
</details>
---

## Ejercicio

### Sistema de Caja Registradora Automatizada

Se va a programar un sistema de cobro de una tienda local. El programa debe registrar las compras de un cliente, artículo por artículo, aplicar un descuento si se cumple una condición especial, y detenerse cuando ya no haya más productos por registrar.
Por cada artículo, el programa solicitará el Precio del producto y la Cantidad que lleva el cliente.

Para incentivar las compras grandes, la tienda aplica una promoción:

* Descuento del 15%: Si el precio del producto es mayor a $20 y la cantidad de unidades de ese mismo producto es mayor o igual a 3.Sin descuento: Si no se cumplen ambas condiciones, el producto se cobra a precio normal (Precio * Cantidad).
* El programa debe usar un bucle para permitir al usuario ingresar un producto tras otro.

* En cada iteración, el sistema debe calcular el subtotal de ese producto (aplicando el descuento si corresponde) e irlo sumando a una variable acumuladora llamada total_pagar.

* El bucle continuará repitiéndose mientras el Precio del producto ingresado sea mayor que 0. Si el usuario ingresa un precio de 0, el programa entiende que la compra terminó.

* Al salir del bucle, el programa debe mostrar en pantalla el valor final que el cliente debe cancelar.


---

## Portafolio 
<p align="center">
*<strong><a href="Portafolio.md">INICIO</a></strong>*
</p>
