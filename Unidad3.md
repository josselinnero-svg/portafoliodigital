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
* En la función main: Se pide al usuario que ingrese el precio de un artículo (un float).

* Crear la función aplicarIVA:

* Se debe recibir el precio por valor (float precio).

* Adentro, calcular el precio final sumándole el 15% de IVA (multiplicar por 1.15).

* Debe retornar (return) el nuevo precio.

* En el main: Recibe ese resultado, se muéstra en pantalla y se verifica que la variable original del precio no cambió.

