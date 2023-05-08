- **Login UOC:** sforjab

- **Nombre y apellidos del alumno:** Sergio Forja Barriga

- **Descripción del trabajo realizados en esta PEC:** 

    Esta PEC ha consistido en la realización de distintos ejercicios teórico/prácticos con varios apartados. Pasamos a describir el trabajo realizado en cada uno de ellos.

***

## **Ejercicio 1 - Instalación y configuración de Angular CLI** 

En este ejercicio hemos tenido que contestar una pregunta teórica ('PEC4_Ej_Teor/PEC4_Ej1_respuestas_teoria.md') en la que se pedía explicar la función de distintas opciones de Angular CLI.

***

## **Ejercicio 2 – Hola Mundo con Angular** 

En esta actividad hemos creado el directorio 'PEC4_Ej_Prac' con el fichero 'PEC4_Ej2_respuestas_estructura.md', donde respondemos a varias preguntas teóricas acerca de la creación de un proyecto Angular.

Además de las respuestas a la teoría, hemos ido siguiendo los pasos indicados para crear un proyecto Angular desde cero, el cual continuaremos desarrollando en los siguientes ejercicios.

Nota: Hay que indicar que se han introducido comentarios explicativos en los fragmentos de código más importantes.

***

## **Ejercicio 3 – Primer componente en Angular** 

Este ejercicio consistía en la generación mediante Angular CLI de un primer componente llamado 'article-item'. Se indica la información que debe mostrar y el modelo a crear. 

También se pide resaltar los artículos en venta con un color diferente usando una condición lógica en la plantilla.

Por último, ha sido necesario crear una botonera que permita decrementar e incrementar la cantidad seleccionada del artículo y hemos deshabilitado el botón de decremento cuando la cantidad seleccionada era 0.

***

## **Ejercicio 4 – Directivas de atributo y directivas estructurales** 

Este es un ejercicio teórico consistente en responder distintos apartados relacionados con las directivas de atributo y estructurales de Angular. Dichas respuestas podemos encontrarlas en el fichero 'PEC4_Ej4_respuestas_teoria.md', dentro de la carpeta 'PEC4_Ej_Teor'.

***

## **Ejercicio 5 – Directivas en nuestro proyecto**

Esta actividad nos pedía hacer uso en el proyecto 'ecommerce' de dos tipos de directivas. En primer lugar, de la directiva de atributo 'ngClass' para mostrar el precio en gris si el artículo no está disponible para la venta. Por otra parte, había que utilizar la directiva estructural 'ngIf', para ocultar la botonera (incrementar/decrementar) y la cantidad seleccionada en caso de que el artículo no esté a la venta.

***

## **Ejercicio 6 – Teoría de componentes**

Se nos pide crear en 'PEC4_Ej_Teor' un fichero llamado 'EC4_Ej6_respuestas_teoria.md', donde hemos respondido varias preguntas sobre los componentes: encapsulación de estilos, mecanismo de detección de cambios, etc.

***## **Ejercicio 7 - Componentes en nuestro proyecto**

Por último, se nos indicaban varios requisito más que era necesario añadir a nuestro proyecto Angular 'ecommerce'. Estos requisitos, en resumen, han sido:

- Crear un nuevo componente 'article-list', cuya plantilla utiliza ladirectiva estructural 'ngFor' para crear un 'article-item' por cada uno de los tres artículos existentes.
- Utilizar templates y estilos en línea para 'article-item'.
- Modificar 'article-item' para recibir como entrada un 'Article' y para que emita hacia el padre un objeto 'ARticleQuantityChange' (artículo y cantidad de unidades seleccionadas).
- Modificar la lógica de decrementar/incrementar del 'article-item' para añadirla a 'article-list' y utilizar un 'id' para encontrar un artículo y cambiar su cantidad.
- Modificar 'article-item' para que su estrategia 'ChangeDetection' sea óptima.

Como dijimos anteriormente, en el código pueden encontrarse comentarios de los puntos más relevantes de los ejercicios.