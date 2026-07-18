## Unidad 3
## Modularidad
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
* 

</blockquote>
</details>
  
