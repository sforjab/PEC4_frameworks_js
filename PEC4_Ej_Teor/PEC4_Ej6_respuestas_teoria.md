**1. ¿Cuáles son los style encapsulation de los componentes? Pon un ejemplo de uso de cada uno de ellos.**

Existen tres tipos de *style encapsulation* para componentes:

- *Emulated*: es el encapsulamiento de estilos por defecto. Angular genera selectores CSS únicos para cada componente y se aplican como atributos de los elementos HTML de la vista (template) de éste. De esta manera, no afectan a otros elementos de la aplicación, emulando el comportamiento del Shadow DOM.
  
  Un ejemplo sería el siguiente:
  ```
    import { Component, ViewEncapsulation } from '@angular/core';

    @Component({
        selector: 'app-emulated',
        templateUrl: './emulated.component.html',
        styleUrls: ['./emulated.component.css'],
        encapsulation: ViewEncapsulation.Emulated
    })
    export class EmulatedComponent {
        // ...
    }
  ```

- *Native*: este tipo, emplea las funcionalidades de encapsulamiento proporcionadas por el navegador, lo que quiere decir que los estilos definidos dentro del componente, solamente afectarán a los elementos dentro del *shadow root* del mismo, independizando sus estilos de los del resto de la aplicación.
  
  Vemos un ejemplo:

  ```
  import { Component, ViewEncapsulation } from '@angular/core';
  @Component({
    selector: 'app-native',
    templateUrl: './native.component.html',
    styleUrls: ['./native.component.css'],
    encapsulation: ViewEncapsulation.Native
  })
  export class NativeComponent {
    // ...
  }
  ```

- *None*: esta opción hace que los estilos se apliquen de forma global, es decir, los estilos definidos en un componente se aplicarán a todos los elementos HTML que coincidan con el selector CSS, sin tener en cuenta si están dentro o fuera del mismo.
  
  Los vemos en el siguiente ejemplo:

  ```
  import { Component, ViewEncapsulation } from '@angular/core';

  @Component({
    selector: 'app-none',
    templateUrl: './none.component.html',
    styleUrls: ['./none.component.css'],
    encapsulation: ViewEncapsulation.None
  })
  export class NoneComponent {
    // ...
  }
  ```

***

**2. ¿Qué es el shadow DOM?**

Es una característica de los navegadores web que permite encapsular código HTML, CSS y JavaScript dentro de un componente web, de forma que no interactúe con el resto de la página. Esto se consigue creando un árbol DOM independiente del DOM principal de la web, logrando así que el contenido y los estilos de los componentes anidados en el *Shadow DOM* no puedan ser accedidos desde fuera de su ámbito.

***

**3. ¿Qué es el changeDetection?**

Se trata del mecanismo empleado por Angular para detectar los cambios en los datos y renderizar la vista en función de dichos cambios. 

Se ejecuta de forma automática al completarse ciclos de eventos y por defecto, utiliza una estrategia (*Change​DetectionStrategy.Default*) consistente en comparar la referencia de los objetos para comprobar si se han producido cambios.

***

**4 ¿Qué diferencias existen entre las estrategias Default y OnPush?**

La estragia *Default* hace que cada vez que se produzca un evento, Angular compruebe todos los componentes para ver si hay algún cambio y actualice los estados si se requiere. Por el contrario, con la entrategia *OnPush*, Angular solamente comprueba los cambios existentes cuando se produce un cambio en una entrada de datos.

**¿Cuándo debes usar una y otra?**
Debemos usar la estrategía *default* cuando las aplicaciones sean pequeñas o medianas, o en caso de que los componentes cambien con frecuencia. La estrategia *OnPush* es adecuada para aplicaciones complejas o de gran tamaño, ya que mejora el rendimiento de las mismas.

**Ventajas e inconvenientes**
La estrategia *default* conlleva un proceso más costoso que puede afectar al rendimiento de la aplicación. Sin embargo, su implementación es más sencilla. 

Por su parte, la estrategia *OnPush* mejora el rendimiento de las aplicaciones con muchos componentes. En cambio, se requiere un mayor esfuerzo de programación para configurar y es posible que sea difícil de comprender para desarrolladores no expertos.

***

**5. Explica con detalle el ciclo de vida de los componentes. Haz hincapié en cuándo se disparan los hooks OnChanges, OnInit, AfterViewInit y OnDestroy, puesto que son los más utilizados**

El ciclo de vida de un componente Angular consiste en un proceso ordenado de eventos que se producen desde la creación hasta la destrucción del componente. Estos eventos son los siguientes:

- ```Costructor```: es lo primero que se llama al crear el componente e inicializa las propiedades de la clase.
- ```ngOnChanges```: este hook se dispara cada vez que se detectan cambios en las propiedades de entrada (@Input), justo antes de que se renderice el componente con los nuevos valores de las propiedades actualizadas. Recibe un objeto *SimpleChanges* que contiene los cambios en las entradas del componente. Esta información se puede utilizar para comprobar si se han producido cambios en las entradas y realizar alguna acción en consecuencia.
- ```ngOnInit```: se ejecuta una única vez, tras la llamada del constructor del componente (tras inicializar todas las propiedades) y antes de que éste se renderice en la vista. Realiza tareas de inicialización adicionales, como pueden ser la carga de datos o las llamadas a servicios.
- ```ngDoCheck```: su función es detectar y responder a cambios personalizados en el componente que no son detectados por el *changeDetection* de Angular.
- ```ngAfterContentInit```: se ejecuta tras la inicialización del contenido proyectado en el componente y realiza acciones que dependan de dicho contenido.
- ```ngAfterContentChecked```: una vez que el contenido del componente se verifica para cambios, se ejecuta para permitir al componente realizar cualquier acción necesaria derivada de dichos cambios.
- ```ngAfterViewInit```: este hook se ejecuta un única vez, cuando el componente y sus vistas han sido inicializados. Es empleado con frecuencia para tareas que requieren acceso a elementos del DOM.
- ```ngAfterViewChecked```: es llamado cada vez que se realiza una comprobación de cambio en la vista de un componente, por lo que es útil para tareas que deban realizarse tras la actualización de la vista.
- ```ngOnDestroy```: este hook se dispara justo antes de la destrucción del componente. Básicamente, su función es la de liberar recursos, por lo que es importante su uso para poder evitar problema de memoria.