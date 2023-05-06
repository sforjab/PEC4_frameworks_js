**Explica qué hace cada una de las siguientes opciones de Angular CLI:**


- ``` ng new ```: sirve para crear un nuevo proyecto Angular, incluyendo la estructura de directorios y archivos de configuración, componentes, servicios, módulos y otros ficheros necesarios.
  
- ``` ng generate ```: sirve para generar distintos tipos de archivos utilizados en un proyecto Angular. A continuación vemos qué tipo de ficheros podemos generar.
  - ``` component ```: genera un nuevo componente en nuestro proyecto, creando los ficheros que contendrán la lógica, la vista, los estilos y las pruebas automatizadas. También actualizará el archivo *app.module.ts* para registrar el nuevo componente, estando así disponible en la aplicación.
  - ``` directive ```: genera una nueva directiva en el proyecto, creando los ficheros que contienen la lógica y las pruebas automatizadas. La registra también actualizando el fichero *app.module.ts*.
  - ``` enum ```: sirve para generar archivo de enumeración en el proyecto. Al ejecutarlo, crea un fichero que contiene la definición de la enumeración. Actualiza el archivo *app.module.ts* para registrar la enumeración.
  - ``` guard ```: genera en el proyecto un *guard*, que es una clase para controlar el acceso a rutas y componentes según ciertas condiciones. Crea un fichero con la lógica del *guard* y otro con las pruebas automatizadas. Es registrado automáticamente modificando el fichero *app.module.ts*.
  - ``` interface ```: se utiliza para generar una interfaz en el proyecto, creando el fichero que contiene su definición.
  - ``` pipe ```: genera un nuevo *pipe* en el proyecto, es decir, una clase para transformar datos antes de mostrarlos en la vista. Crea el fichero que contendrá la lógica y el de las pruebas automatizadas. Modifica también el dichero *app.module.ts* para registrar el *pipe*.
  - ``` service ```: sirve para generar un nuevo servicio en el proyecto. Para ello crea los ficheros de la lógica y las pruebas y modifica el *app.module.ts* para registrar el nuevo servicio.

- ``` ng serve ```: esta orden sirve para compilar y ejecutar la aplicación Angular en un servidor de desarrollo local, abriéndola en el navegador. Dispone de recarga automática, es decir, detecta cualquier modificación del código y actualiza el navegador sin tener que reiniciar el servidor.
  
- ``` ng test ```: con este comando se ejecutan las pruebas automatizadas del proyecto. También utiliza la recarga automática, ejecutando las pruebas de nuevo al detectar cambios en el código.

- ``` ng version ```: sirve para imprimir la versión actual de Angular CLI y de las distintas dependencias que se utilizan en el proyecto.