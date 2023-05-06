**1. Explica qué son y cuándo se deberían utilizar las siguientes variables locales de la directiva estructural ```NgFor```.**

- ```index```: es el índice del elemento actual en el bucle. Podemos usarlo para acceder a elementos de otras listas o para realizar algún tipo de cálculo.
  
- ```even```: se trata de una variable booleana que es *true* cuando el índice es par. Por lo tanto, deberíamos usarlo en situaciones en las se quiera comprobar si un elemento es par o en aquellas en las que se desee realizar acciones diferentes para elementos pares e impares, como por ejemplo, aplicar estilos distintos.

- ```odd```: también es una variable booleana, pero en esta ocasión es *true* cuando el índice es impar. Lo usaríamos para los mismos supuestos que ```even```, teniendo en cuenta que en este caso vamos a comprobar si el elemento es impar.

- ```first```: es una variable booleana cuyo valor es *true* si el elemento actual es el primer elemento de la lista. Deberíamos usarlo cuando queramos realizar alguna acción sobre el primer elemento, como por ejemplo, modificar el valor de una variable solamente para ese elemento.

- ```last```: esta variable también es booleana, pero es *true* cuando el elemento actual es el último elemento de la lista. Se usaría para los mismos supuestos que ```first```, pero teniendo en cuenta que las acciones se van a realizar sobre el último elemento.

***

**2. ¿Para qué sirve la opción trackBy de la directiva estructural NgFor? Pon ejemplos de uso.**

Con esta opción podemos optimizar el rendimiento a la hora de renderizar las listas. 

Esto es debido a que al usar ```NgFor```, Angular identifica a cada elemento de la lista por su índice, pero al modificarla, renderiza de nuevo todo el contenido incluso si no ha cambiado. 

Al usar ```trackBy```, podemos proporcionar a Angular una función para que identifique los elementos por una clave única en lugar del índice, por lo que podrá detectar y actualizar únicamente los que hayan sido modificados, mejorando el rendimiento de la aplicación.

***

**3. ¿Es posible ejecutar dos directivas estructurales simultáneamente? Explica la razón tanto si es si posible como si no lo es.**

No es posible utilizar dos directivas estructurales en el mismo elemento HTML al mismo tiempo, ya que pueden producirse problemas de ambigüedad. Cuando usamos una directiva estructural, estamos manipulando la estructura del DOM, por lo que al usar dos directivas juntas Angular no sabría cuál ejecutar primero.