## Unidad 2

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

<img width="499" height="250" alt="image" src="https://github.com/user-attachments/assets/d5de49c9-e085-47d1-b12f-8db4522ca752" />


* Hacer Mientras (Do-While): Similar al "mientras", pero las instrucciones se ejecutan al menos una vez, ya que la condición se evalúa al final

Diagrama de flujo: El bloque de instrucciones va primero, seguido por el rombo de condición

<img width="342" height="356" alt="image" src="https://github.com/user-attachments/assets/e87aa1f9-2fcc-4af2-acd7-f7914f3cf0c7" />

Pseudocódigo: Hacer Realizar instrucciones Mientras condición Fin Mientras

<img width="436" height="283" alt="image" src="https://github.com/user-attachments/assets/2abf2476-4926-4697-853f-b4e52890efae" />


* Desde/Para (For): Se utiliza cuando se conoce de antemano el número de iteraciones. Utiliza una variable índice, un valor inicial y un valor final
Diagrama de flujo: Incluye la inicialización del índice, la comparación con el valor final, la ejecución de instrucciones y el incremento automático del índice.

<img width="475" height="367" alt="image" src="https://github.com/user-attachments/assets/24eceabf-396f-4d5a-9a7b-56f74683262b" />

Pseudocódigo: para vo asignar vi hasta vf incrementar hacer realizar instrucciones fin para

<img width="470" height="196" alt="image" src="https://github.com/user-attachments/assets/4d8a9868-3b11-4600-a5e4-65ee0189bd44" />

  
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

Identificamos los datos de entrada  y elaboramos el codigo en C 
```c
#include <stdio.h>

int main () {
    int cantidad;
    float precio, subtotal, total_pagar = 0;

    do {
        printf("Ingrese precio de producto: \n");
        scanf("%f", &precio);

        if (precio != 0) {
            printf("Ingrese cantidad: \n");
            scanf("%i", &cantidad);

            subtotal = precio * cantidad;

            if (precio > 20 && cantidad >= 3) {
                subtotal = subtotal * 0.85;
                printf("-> Descuento aplicado.\n");
            }

            total_pagar = total_pagar + subtotal;
            printf("Subtotal actual de la compra: $%.2f\n", total_pagar);
        }

    } while (precio != 0);

    printf("\n=============================================\n");
    printf("Monitoreo de caja finalizado.\n");
    printf("El precio del producto sin el descuento: $%.2f\n", subtotal);
    printf("El descuento aplicado en ese producto: %.2f*0.85 \n", subtotal);
    printf("El total neto a pagar es: $%.2f\n", total_pagar);
    printf("=============================================\n");

    return 0;
}
```

### Diagrama de flujo 

<img width="3684" height="3964" alt="image" src="https://github.com/user-attachments/assets/cafd8c29-d201-4263-9971-eedc4f1faf35" />


#### Prueba de Escritorio - Simulador de Caja Registradora


A continuación se detalla el seguimiento paso a paso de las variables durante la ejecución del programa basándose en los datos ingresados en la terminal.

| Iteración | Entrada: Precio (`precio`) | Entrada: Cantidad (`cantidad`) | Condición Descuento (`precio > 20 && cantidad >= 3`) | Subtotal del Artículo | Acumulador: Total a Pagar (`total_pagar`) |
| :---: | :---: | :---: | :---: | :---: | :---: |
| **Inicio** | - | - | - | - | $0.00 |
| **1** | 10.0 | 3 | Falso (Precio no es > 20) | 10 * 3 = **30.00** | 0.00 + 30.00 = **30.00** |
| **2** | 30.0 | 3 | **Verdadero** (Aplica 15%) | (30 * 3) * 0.85 = **76.50** | 30.00 + 76.50 = **106.50** |
| **3** | 40.0 | 2 | Falso (Cantidad no es >= 3) | 40 * 2 = **80.00** | 106.50 + 80.00 = **186.50** |
| **4** | 10.0 | 20 | Falso (Precio no es > 20) | 10 * 20 = **200.00** | 186.50 + 200.00 = **386.50** |
| **5** | 35.0 | 5 | **Verdadero** (Aplica 15%) | (35 * 5) * 0.85 = **148.75** | 386.50 + 148.75 = **535.25** |
| **6** | 0.0 | - | No evalúa (Condición de parada) | - | **Sigue en $535.25** (Fin del bucle) |

**Resultado final en pantalla:** El total neto a pagar es: **$535.25**

Tenemos la comprobación de la ejecución del programa 

<img width="831" height="876" alt="image" src="https://github.com/user-attachments/assets/c23c0259-5253-4e12-a772-8de7448944fc" />

---

### 📝 Conclusión

<table>
<tr>
<td>
<strong>Principales Dificultades</strong><br><br>
La mayor dificultad radicó en la integración de estructuras, específicamente al anidar el bloque <code>if/else</code> dentro del bucle <code>while</code>. Lograr que el programa tomara decisiones lógicas (condicionales) de forma repetitiva sin perder el control del flujo o generar errores en los cálculos acumulados representó un reto de abstracción importante. También fue complejo asegurar que la condición de parada del bucle no fuera procesada accidentalmente por la lógica del <code>if</code>.
</td>
</tr>
</table>

---

### 💡 Reflexión Crítica

<table>
<tr>
<td>
El uso combinado de bucles y condicionales es lo que permite crear programas dinámicos y útiles. A pesar de la dificultad inicial, se comprendió que la programación real consiste en gestionar estados: el <code>while</code> mantiene el sistema activo, mientras que el <code>if</code> gestiona las reglas del negocio. Esta práctica fue clave para desarrollar un pensamiento lógico más estructurado, pasando de seguir instrucciones simples a diseñar procesos automáticos que reaccionan a diferentes entradas del usuario.
</td>
</tr>
</table>

---

## Indice
<p align="center">
*<strong><a href="index.md">ÍNDICE</a></strong>*
</p>
