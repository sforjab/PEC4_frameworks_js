**1. ¿Qué comando debes utilizar para crear un nuevo proyecto Angular utilizando Angular CLI denominado ecommerce?**

```
ng new ecommerce
```

**Explica brevemente la estructura y ficheros que ha generado Angular CLI:**

**Ficheros de configuración en la raíz del proyecto**
  
  - ```.editorconfig```: se trata de un fichero cuya finalidad es definir y estandarizar la configuración del editor de código usado en un proyecto Angular.
  - ```.gitignore```: este archivo indica a Git qué ficheros y carpetas deben ser ignorados por el sistema de control de versiones, evitando su inclusión en el repositorio.
  - ```angular.json```: archivo donde se definen aspectos del proyecto Angular, como por ejemplo, opciones de compilación, dependencias, rutas, etc.
  - ```package-lock.json```: es un archivo de bloqueo de versiones y sirve para garantizar que se instalen las versiones exactas de las dependencias especificadas en el fichero *package.json*.
  - ```package.json```: este fichero se utiliza para definir las dependencias, scripts y metadatos de la aplicación.
  - ```tsconfig.json```: este archivo se emplea para configurar el compilador de TypeScript para todo el proyecto.
  - ```tsconfig.app.json```: fichero que especifica cómo debe TypeScript compilar y generar el código JavaScript de la aplicación Angular. La diferencia con el anterior es que en este caso, la configuración del compilador TypeScript se realiza específicamente para la parte de la aplicación que se construye y ejecuta en el navegador.
  - ```tsconfig.spec.json```: este archivo sirve para especificar la configuración del compilador de TypeScript para las pruebas unitarias de la aplicación.  


**Directorio node_modules**

Este directorio contiene las dependencias del proyecto y su módulos y es utilizado por Angular para copilar y construir la aplicación.

**Directorio src**
  
  - ```favicon.ico```: imagen empleada por los navegadores como icono de la web. Puede verse en la pestaña del navegador al cargar.
  - ```index.html```: es el archivo principal de la aplicación y en él se cargan los ficheros necesarios para poder ejecutarla, incluyendo JavaScript, CSS, etc.
  - ```main.ts```: en este archivo se realiza la inicialización y configuración básica de la aplicación Angular y sirve como punto de entrada a la misma.
  - ```styles.css```: en este fichero se definen los estilos de la aplicación.
  - Directorio ```assets```: en este directorio se almacenan los archivos estáticos que se utilizarán en la aplicación, como imágenes, fuentes, etc. Por defecto, contiene un fichero llamado ```.gitkeep```, que es un archivo vacío utilizado para mantener un directorio vacío en un repositorio Git.
  - Directorio ```app```: en este directorio se almacenan los componentes, módulos, servicios, etc., es decir, los ficheros que definen la lógica de la aplicación. Dentro encontramos:
    - ```app.component.css```: es la hoja de estilos asociada al componente raíz de la aplicación (*AppComponent*).
    - ```app.component.html```: es el archivo de plantilla asociado al componente raíz de la aplicación. Contiene el código HTML y las directivas Angular que definen la estructura y el contenido de la página principal de la aplicación.
    - ```app.component.spec.ts```: es el fichero de test del componente raíz de la aplicación. Contiene pruebas unitarias que verifican si el componente funciona correctamente y cumple los requisitos de la aplicación.
    - ```app.component.ts```: es un fichero que define la lógica y el comportamiento del componente raíz de la aplicación Angular. Es el primer componente que se carga al iniciar la aplicación.
    - ```app.module.ts```: define el módulo raíz de una aplicación Angular. En este fichero se importan y exportan los componentes, servicios y otros elementos requeridos por la aplicación.

**Ficheros y directorios no generados**

Al realizar la generación de nuestro nuevo proyecto Angular 'ecommerce' (versión de Angular CLI 15.2.7), no se han generado algunos ficheros o directorios de ```src`` de los especificados en el enunciado del ejercicio. Son los siguientes:

- ```test.ts```
- ```polyfills.ts```
- Directorio ```environments```
  
***

**2. Explica cada uno de los siguientes decoradores generados por Angular CLI, detallando cada una de las propiedades que se definen en:**

**app.module.ts** - ```@NgModule```: este decorador es empleado para marcar una clase que define un módulo de Angular. Este módulo puede contener componentes, directivas, servicios, etc.
  - ```declarations```: define las directivas, componentes y pipes que pertenecen al módulo y que se van a utilizar en la aplicación.
  - ```imports```: define los módulos que se van a importar al módulo actual.
  - ```providers```: define los servicios que se van a utilizar en al aplicación o en algún módulo concreto.
  - ```bootstrap```: define el componente raíz que se utiliza como punto de entrada a la aplicación, es decir, el componente que se va a cargar en la página principal.

**app.component.ts** - ```@Component```: este decorador se utiliza para definir componentes, cuya configuración se basa en las siguientes propiedades:
  - ```selector```: define el selector CSS que se va a utilizar para seleccionar el componente en el HTML.
- ```templateUrl```: define la ubicación de la plantilla del componente (archivo HTML).
- ```styleUrls```: es un array que contiene las ubicaciones de los archivos CSS que se van a emplear para dar estilo a la aplicación.
  
***

**3. ¿Es posible poder inyectar el template y los estilos en línea de un componente sin necesidad de especificarlos en templateUrl, styleUrls?**

Sí, es posible.

Para inyectarlos en línea emplearíamos en el decorador ```@Component``` los parámetros *template* y *styles* en lugar de *templateUrl* y *styleUrls*. Para la propiedad *template*, el valor será una cadena que contiene el HTML. Para la propiedad *styles*, el valor será un array conlas distintas reglas CSS que se aplicarán.

**¿Es recomendable hacer esto?**

En general no es recomendable. 

Es cierto que, en determinados casos, si las plantillas y los estilos no tienen mucha complejidad y son específicas del componente, puede tener sentido inyectarlos en línea.

Sin embargo, cuando aumenta la complejidad o se utilizan en varios componentes, lo idóneo es separarlos en archivos independientes. Por lo que por regla general se recomienda hacer esto último, ya que ayuda a que el código sea más legible y quede mejor organizado.
