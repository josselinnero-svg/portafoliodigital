## Unidad 3  🧩
# Modularidad
La modularización es una técnica de programación orientada a reducir la complejidad de algoritmos largos y complejos mediante la división de un programa grande en subprogramas más pequeños, bajo el principio de "divide y vencerás"
* Módulos: Estos subprogramas reciben nombres como funciones, procesos, rutinas o sub-rutinas
* Funciones: Son conjuntos de sentencias que realizan una tarea única e identificable. 
No pueden ejecutarse por sí solas; deben estar ancladas a un programa principal (como el main). 
Constan de una cabecera (tipo de retorno, nombre y parámetros) y un cuerpo (sentencias y valor de retorno)
* Procedimientos: Son funciones que no utilizan la instrucción return (no devuelven valores) ni reciben parámetros

<details>
<summary><b>🪼 Pase de parámetros </b></summary>
<blockquote>
Existen dos formas teóricas de enviar datos a un módulo:
  
* Pase por valor (Ejemplo): Se envía únicamente el contenido de la variable (por ejemplo, el valor 5). La función utiliza este dato en sus instrucciones, pero la variable original fuera de la función no se altera
* Pase por referencia (Ejemplo): Se envía la dirección de memoria de la variable. Esto implica que cualquier cambio realizado dentro de la función afectará directamente a la variable original fuera de ella

</blockquote>
</details>

# Arreglos (Arrays)
Los arreglos son estructuras de datos estáticas donde cada dato individual se denomina elemento
* Facilitan el acceso a la información mediante el uso de índices, los cuales siempre comienzan en la posición cero
<details>
<summary><b>🪼 Tipos de arreglos y su representación teórica </b></summary>
<blockquote>
  
* Unidimensionales (Vectores o Listas):

  Teoría: Tienen una sola fila y varias columnas.
  
  Ejemplo de sintaxis: <tipo dato> <identificador> [<núm_elemen>]; por ejemplo: int num
  o char letras.
  
* Bidimensionales (Matrices):
  
  Teoría: Se componen de varias filas y varias columnas.
  
  Ejemplo de representación: Se identifican como m[i][j], donde i representa el número de filas y j el número de columnas (ej. int prueba).
  
* Multidimensionales (Tridimensionales):
  
  Teoría: Incluyen filas, columnas y una dimensión adicional de profundidad.
  
  Ejemplo de representación: Se definen como m[i][j][k], donde i es la profundidad, j las filas y k las columnas

</blockquote>
</details>

# EJERCICIOS
## Modularidad 📎

### Ejercicio 1: Por Valor (El Calculador de Descuentos) 🏷️
En este ejercicio, la función recibe una copia del precio, calcula el descuento y te devuelve el nuevo precio sin modificar la variable original en el main.

Instrucciones:
* En la función main: Pide al usuario que ingrese el precio de un artículo (un float).

* Crea la función aplicarDescuento:

* Debe recibir el precio por valor (float precio).

* Adentro, calcula el precio final restándole el 15% de descuento (multiplicar por 0.85).

* Debe retornar (return) el nuevo precio.

* En el main: Recibe ese resultado, muéstralo en pantalla y verifica que la variable original del precio no cambió.

 Tenemos el siguiente codigo en C 

```c
#include <stdio.h>

// Prototipo de la función
float aplicarDescuento(float precio);

int main() {
    float precioOriginal, precioFinal;

    printf("=== PASO POR VALOR: CALCULADOR DE DESCUENTO ===\n");
    printf("Ingrese el precio del producto: $");
    scanf("%f", &precioOriginal);

    // Se pasa la variable 'precioOriginal' por valor
    precioFinal = aplicarDescuento(precioOriginal);

    printf("\nResultados:\n");
    printf("Precio original en main: $%.2f\n", precioOriginal);
    printf("Precio final con 15%% de descuento: $%.2f\n", precioFinal);

    return 0;
}

// Función que recibe por VALOR
float aplicarDescuento(float precio) {
    float resultado;
    resultado = precio * 0.15 ; // Aplica un 15% de descuento
    return resultado;
}

* En el main: Recibe ese resultado, se muéstra en pantalla y se verifica que la variable original del precio no cambió.

```

Este es el resultado en la terminal

<img width="268" height="75" alt="image" src="https://github.com/user-attachments/assets/fdb772cb-7673-4e7b-be67-06b008e794ee" />

### Ejercicio 2: Paso por Referencia (Transmutador Alquímico)

* **Concepto:** Modificación directa de recursos en memoria sin usar `return`.
* **Descripción:** Una función convierte monedas de plata en oro (10 de plata = 1 de oro) alterando directamente los valores almacenados en las direcciones de memoria de la billetera.

```c
#include <stdio.h>

// Prototipo de la función (recibe por REFERENCIA las monedas)
void transmutarMonedas(int *ptrOro, int *ptrPlata);

int main() {
    int misMonedasOro = 5;
    int misMonedasPlata = 34;

    printf("=== BILLETERA ALQUÍMICA (PASO POR REFERENCIA) ===\n");
    printf("Antes del hechizo:\n");
    printf("Oro: %i | Plata: %i\n", misMonedasOro, misMonedasPlata);

    // Pasamos las direcciones de memoria de la billetera con '&'
    transmutarMonedas(&misMonedasOro, &misMonedasPlata);

    printf("\nDespues del hechizo (10 de plata = 1 de oro):\n");
    printf("Oro: %i | Plata: %i\n", misMonedasOro, misMonedasPlata);

    return 0;
}

// La función convierte cada 10 monedas de plata en 1 de oro
void transmutarMonedas(int *ptrOro, int *ptrPlata) {
    int oroNuevo = *ptrPlata / 10;   // Calcula cuánto oro sale
    *ptrPlata = *ptrPlata % 10;      // Deja el residuo
    *ptrOro = *ptrOro + oroNuevo;    // Modifica el oro original en memoria
}
```
Este es el resultado en la terminal

<img width="280" height="79" alt="image" src="https://github.com/user-attachments/assets/d8f56a98-7ba3-4dbb-ba54-c50c3077cdab" />



# Ejercicios de Arreglos (Arrays) en C

Repositorio para practicar el uso y manipulación de arreglos **unidimensionales**, **bidimensionales** y **tridimensionales** en C.

---

## Arreglo unidimensional 
Identificamos los datos de entrada y elaboramos el código para el arreglo **Unidimensional** (Vectores) en C:

```c
#include <stdio.h>

int main() {
    // Declaración e inicialización de un vector de 5 elementos
    float notas[5] = {8.5, 9.0, 7.5, 10.0, 6.0};
    float suma = 0.0, promedio;

    printf("=== ARREGLO UNIDIMENSIONAL (VECTOR) ===\n");
    
    // Recorremos el vector con un solo ciclo for
    for (int i = 0; i < 5; i++) {
        printf("Nota [%i]: %.2f\n", i + 1, notas[i]);
        suma += notas[i];
    }

    promedio = suma / 5;
    printf("\nEl promedio final es: %.2f\n", promedio);

    return 0;
}
 ```
Este es el resultado en la terminal

<img width="203" height="102" alt="image" src="https://github.com/user-attachments/assets/9439a751-f058-469e-aaf5-970402c28dde" />

## Arreglo Bidimensional 

```c
#include <stdio.h>

int main() {
    // Declaración e inicialización de una matriz de 3 filas x 3 columnas
    int matriz[3][3] = {
        {1, 2, 3},
        {4, 5, 6},
        {7, 8, 9}
    };

    printf("=== ARREGLO BIDIMENSIONAL (MATRIZ 3x3) ===\n\n");

    // Recorremos la matriz usando ciclos for anidados
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            printf("%i\t", matriz[i][j]);
        }
        printf("\n"); // Salto de línea por cada fila
    }

    return 0;
}
 ```


Este es el resultado en la terminal

<img width="233" height="72" alt="image" src="https://github.com/user-attachments/assets/35dfb8ea-b61e-401e-bf39-869ef3748d62" />

## Arreglo Tridimensional

```c
#include <stdio.h>

int main() {
    // Arreglo 3D: 2 capas (matrices), 3 filas y 3 columnas
    int cubo[2][3][3] = {
        {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        },
        {
            {10, 20, 30},
            {40, 50, 60},
            {70, 80, 90}
        }
    };

    printf("=== ARREGLO TRIDIMENSIONAL (CUBO) ===\n");

    // Necesitamos 3 ciclos for anidados (capa, fila, columna)
    for (int capa = 0; capa < 2; capa++) {
        printf("\n--- CAPA %i ---\n", capa + 1);
        for (int fila = 0; fila < 3; fila++) {
            for (int col = 0; col < 3; col++) {
                printf("%i\t", cubo[capa][fila][col]);
            }
            printf("\n");
        }
    }

    return 0;
}
 ```

Este es el resultado en la terminal

<img width="203" height="140" alt="image" src="https://github.com/user-attachments/assets/1700660e-5bd3-4abf-b72e-fa2e8b895e31" />



### 🔴 Principales dificultades
* **Confusión conceptual en la modularidad:** Al inicio se me complicó un poco aplicar la modularidad de forma limpia, ya que tendía a mezclar varios conceptos al mismo tiempo (como el uso adecuado de parámetros por valor vs. por referencia, el manejo de punteros `*` y `&`, y cuándo una función debía retornar un valor o ser de tipo `void`).
* **Control de índices en arreglos multidimensionales:** En la transición hacia arreglos bidimensionales y tridimensionales, el manejo de múltiples ciclos de lectura y recorrido anidados (`for`) representó un reto para no perder el rastro del orden correcto de capas, filas y columnas.

### 💡 Reflexión crítica
El desarrollo de estos ejercicios me permitió comprender que escribir código funcional no es suficiente; la **estructuración y legibilidad** son aspectos fundamentales en la ingeniería de software. La modularidad no solo ayuda a desglosar problemas complejos en partes más pequeñas y manejables, sino que también facilita enormemente la depuración y reutilización del código. 

Aprender a diferenciar entre el paso por valor y por referencia me dio una visión más clara de cómo se administra la memoria en C. Asimilar estos conceptos fue clave para abordar los arreglos con mayor lógica, pasando de una programación lineal a una estructura mucho más ordenada, escalable y mantenible.

---

## Indice
<p align="center">
*<strong><a href="index.md">ÍNDICE</a></strong>*
</p>
