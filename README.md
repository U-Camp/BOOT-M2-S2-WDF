![Banner](imagenes/banner.png)

# M1S2: CSS y Responsive Design. Git y GitHub.

> #### ¡Hola!, ¿qué tal?, ¿cómo te sientes?, ¿qué te han parecido las clases sabatinas?
> #### Recuerda que, si tienes alguna duda, cuentas con tus coaches que podrán ayudarte al respecto y a quienes les podrás escribir desde la pestaña publicaciones en Teams para aclarar las dudas que tengas.
> #### A continuación, seguimos con el contenido correspondiente a la semana 2, en donde revisaremos algunos temas de CSS.
> #### Iniciemos…


## **ÍNDICE**

* [CSS: Responsive Design](https://github.com/U-Camp/BOOT-M1-SEM2#css-responsive-design)
  * [Media Queries](https://github.com/U-Camp/BOOT-M1-SEM2#media-queries)
* [CSS: Frameworks](https://github.com/U-Camp/BOOT-M1-SEM2#css-frameworks)
  * [Bootstrap](https://github.com/U-Camp/BOOT-M1-SEM2#bootstrap)
* [CSS: Transformaciones](https://github.com/U-Camp/BOOT-M1-SEM2#transformaciones)
* [CSS: Transiciones](https://github.com/U-Camp/BOOT-M1-SEM2#transiciones)
* [Git: Sistema de control de versiones](https://github.com/U-Camp/BOOT-M1-SEM2#git-sistema-de-control-de-versiones)
  * [Agregar cambios](https://github.com/U-Camp/BOOT-M1-SEM2#agregar-cambios) 
  * [Confirmar cambios](https://github.com/U-Camp/BOOT-M1-SEM2#confirmar-cambios) 
* [GitHub: Plataforma para colaboración de software](https://github.com/U-Camp/BOOT-M1-SEM2#github-plataforma-para-colaboraci%C3%B3n-de-software)
<!--[Agile]()-->

# CSS: Responsive Design

Trabajar en la web nos obliga a considerar siempre a nuestros usuarios y a los dispositivos en los cuales consumirán nuestras aplicaciones.

Cabe destacar que, cuando empezamos a diseñar para diferentes dispositivos el área de trabajo es inmensa. Sólo consideraremos lo que tenemos involucrado:

- Móviles, 
- Tabletas, 
- Computadoras,  
- Monitores largos, 
- Televisiones, 
- Pantallas de cine, entre otras.

Para ello, dentro de CSS, podemos encontrar estructuras que permitan flexibilidad. De acuerdo al comportamiento y el dispositivo en el cual el usuario está situado, se contendrán diferentes estilos.

A esta práctica se le conoce como _Responsive Design_, o también, Diseño Responsivo.

El elemento más importante para poder ejecutar esto son los `media queries`.

## Media Queries

Un `media query` se refiere a una regla que incluye un bloque de propiedades CSS si se cumple una condición específica.

Está conformado por:

- `@media`. Indica que aplicaremos un media query.
- `screen`. Indica que estaremos trabajando con pantallas. Existen otras opciones que puedes observar en la [documentación](https://www.w3.org/TR/CSS2/media.html) como `print` o `speech`. Sin embargo, `screen` es indicada para este ejemplo. 
- `&`. Indica que vamos a agregar una condición adicional.
- `max-width: 800px`. Indica que vamos a establecer un límite máximo de 800px como condición. Si la pantalla tiene 800px o menos, se ejecutará ésta. A esto se le conoce como punto de quiebre o `breakpoint`. También existe el contrario que es `min-width`, el cual es la medida mínima.

Ejemplo:
```css
@media screen & (max-width: 800px){
  body{
    background-color: blue;
  }
}
```

Observa en este siguiente ejemplo el cambio con una medida mínima.

```css
@media screen & (min-width: 800px){
  body{
    background-color: blue;
  }
}

```

Dependiendo del dispositivo, se recomienda trabajar en estos rangos:

- 320px — 480px: Dispositivos móviles.
- 481px — 768px: iPads, Tabletas.
- 769px — 1024px: Pequeñas pantallas, computadoras portátiles.
- 1025px — 1200px: Computadoras de escritorio, pantallas amplias.
- 1201px o más: Pantallas extra grandes, televisiones.

Consideraciones importantes:

- CSS trabaja en un formato en cascada. Es decir, tan pronto exista la coincidencia con un `media query` con respecto a las condiciones, se ejecutará esos estilos específicos. 

- Puedes probar tus `media queries` tomando la ventana del navegador y haciendola más pequeña y más grande.

# CSS: Frameworks

CSS cuenta con herramientas adicionales, propuestas por organizaciones o proyectos _Open Source_, que permiten desarrollar con mayor velocidad y bajo una estructura específica.

A estas herramientas se les conocen como _frameworks_.

Uno de los más populares y sólidos es **Bootstrap**.


## Bootstrap

Bootstrap, es un framework front-end basado en CSS y JavaScript, el cual se usa para desarrollar aplicaciones web responsivas, esto es desarrollar páginas y aplicaciones web que se vean bien tanto en escritorio, como en dispositivos móviles (tabletas y celulares). Fue creado por Twitter en 2010 y desde entonces ha gozado de amplia popularidad en el mundo del desarrollo de software, ya que es un framework que es muy fácil de aprender e implementar.

Provee una serie de herramientas que permiten estilizar los elementos HTML, así como plantillas de componentes que ya se encuentran estilizados, tales como fuentes, tipografías, iconos, formularios, botones, tablas, menús de navegación, modales, carruseles de imágenes, así como un amplio abanico de herramientas de JavaScript, las cuales se pueden reusar, ampliando la funcionalidad de cualquier sitio web.

Bootstrap 5 es la versión más reciente y soporta la mayor parte de los navegadores web, excepto por versiones anteriores de IE9, incluyéndose. 

Como ya se comentó, Bootstrap es muy fácil de usar, por lo que cualquier persona con conocimiento básico en HTML y CSS puede implementarla; con su esquema de filas y columnas, permite una responsividad que se ajusta fácil y automáticamente a cualquier tipo de pantalla.

Para poder implementar Bootstrap, se puede hacer de varias maneras:

  **1.	Usando el CDN (Content Delivery Network ) de Bootstrap:** provee la última versión del CSS y del JS de Bootstrap y se incluyen directamente en la página HTML enlazando los archivos necesarios directamente en la etiqueta <HEAD /> de la página.
  
  **2.	Descargando los archivos directamente de la página e incluyéndolos directamente en el paquete de la aplicación***, esto es haciendo referencias igual en el HEAD, pero con enlaces relativos a su ubicación dentro de la página web.
  
  **3.	Instalándolo con “npm”, usando el comando install: `$ npm install bootstrap`.*** Bajo este método se instala en la carpeta `node_modules` del proyecto y se puede referenciar al CSS y al JS directamente importándolos en los archivos en los que se vayan a usar.

Ejemplo:
```html
<!DOCTYPE html>
<html lang="en">
 <head>
   <!-- Última versión del CSS minificado -->
   <link
      rel="stylesheet"   href="https://maxcdn.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css">

   <!-- Última versión del JS minificado -->
   <script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js">
</script>
 </head>
</html>
```

_Ejemplo de Referencias a Bootstrap_

### Filosofía mobile-first en Bootstrap

Se establece que cualquier diseño debe funcionar y ser intuitivo primero en dispositivos móviles y luego en escritorio. 

Para asegurar este comportamiento, se le indica al navegador web el tipo de diseño de la página y el zoom del mismo, por lo que se asigna un metadato en el HEAD de la página para que el explorador actúe de manera adecuada:

Ejemplo:
```html
<meta name="viewport" content="width=device-width, initial-scale=1">
```

### Elementos

La base principal de Bootstrap son los siguientes elementos:

**o	Contenedores:** son elementos que envuelven otros elementos, normalmente son elementos `<div />` a los cuales se le especifica la clase CSS `container` o `container-fluid`. Normalmente a este tipo de contenedores se les pueden asignar otras clases de tal manera que estilen el fondo y el texto de los elementos contenidos, como por ejemplo `bg-dark` o `text-white`.

**o	Grids:**  El sistema de filas y columnas de Bootstrap es su principal cualidad, ya que permite el acomodo de los elementos dentro de una rejilla virtual que se divide en 12 columnas por fila, pudiendo usar tantas filas como sean necesarias para mostrar la página. 

Se usa aplicando las clases `row` y `col`, la clase `col` acepta modificadores dependiendo de las columnas y tamaño del dispositivo, por ejemplo `col-md-4` indica que es una columna de tamaño mediano y que abarca 4 posiciones de las 12 disponibles, pudiendo poner más elementos en las siguientes 8 posiciones que quedan, cambiando el número final de la clase, es decir que por cada fila `row` se pueden poner hasta 12 elementos `col-md-1`, uno por columna o hasta 6 elementos `col-md-2` y así sucesivamente hasta ocupar las 12 posiciones. Normalmente se usan elementos `<div />` para manejar este sistema de filas y columnas.

Ejemplo:
```html
<!DOCTYPE html>
<html lang="en">
 <head>
   <meta charset="UTF-8">
   <meta name="viewport" content="width=device-width, initial-scale=1">
   <title>Ejemplo Bootstrap</title>
   <!-- Última versión del CSS minificado -->
   <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css">
  
   <!-- Última versión del JS minificado -->
   <script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js"></script>
 </head>
 <body>
   <div class="container p-3 my-3 bg-dark text-white">
     <h1>Contenedor</h1>
     <p>Fondo negro y texto blanco.</p>
   </div>
   <div class="container">
     <div class="row">
       <div class="col-md-4">
         <h3>Header de Columna 1</h3>
         <p>Párrafo en columna 1</p>
       </div>
       <div class="col-md-4">
         <h3>Header de Columna 2</h3>
         <p>Párrafo en columna 2</p>
       </div>
       <div class="col-md-4">
         <h3>Header en Columna 3</h3>
         <p>Párrafo en columna 3</p>
       </div>
     </div>
   </div>
 </body>
</html>
```

_Ejemplo de Contenedores y Grid usando Bootstrap_

En el ejemplo, si se renderiza esta página web y luego se le cambia el tamaño, se podrá ver cómo cambian de posición los elementos de tal manera que se adaptan al tamaño del dispositivo en el que se observan. La clase `p-3` indica que se dará un `padding` de 3 pixeles, así mismo la clase `my-3` añade un margen de 3 pixeles.

Básicamente estos son los elementos principales de Bootstrap, se irán conociendo y definiendo más componentes conforme se vaya avanzando en las clases.

>#### ¿Cómo vas?, CSS es super interesante ya que le da más forma a nuestros desarrollos.
>#### Recuerda que si deseas practicar y ver cómo se ve en línea puedes hacerlo en VSC o en https://codepen.io/pen/ solo copiando y pegando el código, así puedes hacer los cambios y pruebas que necesites. ¡Mientras más practiques, más rápido aprenderás!
>#### Seguimos... :relaxed:

### Componentes: Alertas

El componente `alert ` de Bootstrap permite mostrar mensajes al usuario de tal manera que llamen su atención y opcionalmente, que el mismo usuario los pueda quitar de su vista, a manera de notificaciones. Para lograr esto, se usa la clase `alert alert-<tipo>`, donde tipo es el tipo de `alert ` que se va a mostrar, permitiendo 8 distintos tipos (alert-primary, alert-secondary, alert-success, alert-danger, alert-warning, alert-info, alert-light y alert-dark), con lo que se puede estilar cualquier tipo de mensaje.

Ejemplo:
```html
   <div class="mover-elemento borde alert alert-primary">
     Este elemento se movió desde 0,0
     <button type="button" class="close" data-dismiss="alert" aria-label="Close">
       <span aria-hidden="true">&times;</span>
     </button>
   </div>
   ```
_Ejemplo de alert con bootstrap_

# Badges

Los badges  son elementos mayormente visuales que son usados para agregar información adicional a cualquier tipo de contenido. Se usa con la clase `badge` seguida de una clase contextual `badge-<tipo_badge>`, que como ya se ha visto en otros componentes, acepta los mismos 8 posibles valores (badge-primary, badge-secondary, badge-success, badge-danger, badge-warning, badge-info, badge-light y badge-dark).


# Transformaciones

CSS es capaz de realizar transformaciones matemáticas a elementos HTML, esto quiere decir que, aplicando transformaciones, CSS puede mover elementos de una posición X a una posición Y o escalarlos en determinadas proporciones o rotarlos en ciertas direcciones. Para lograr esto, CSS tiene ciertas **"reglas especiales"** que funcionan como métodos de estilo, las cuales permiten realizar este tipo de acciones sobre los elementos y se definen usando la regla `transform ` seguida del método que ejecutará la transformación. De estos métodos los más usados son los siguientes:

  - **translate:** Este método permite mover un elemento a partir de su posición original, de acuerdo a los parámetros dados para el eje X y el eje Y. Ejemplo `transform: translate(50px, 100px);` se mueve el elemento 50 píxeles a la derecha y 100 píxeles hacia abajo. Este método se acompaña con 2 métodos extra `translateX` y `translateY` los cuales permiten mover un elemento en los ejes X y Y respectivamente de manera individual.

  - **rotate:** Permite rotar el elemento en sentido horario o contra-horario, dependiendo de los grados que se le pasen como parámetro. Ejemplo `transform: rotate(45deg);` rota el elemento 45 grados en sentido de las manecillas del reloj (izquierda -> derecha) o `transform: rotate(-45deg);` rota el elemento en 45 grados en sentido contrario a las manecillas del reloj (derecha -> izquierda). Hay métodos extra de rotación, que permiten manejar los 3 ejes, de tal manera que rote el elemento en 3D:

  - **rotateX:** Rota el elemento a determinada cantidad de grados sobre el eje X. Ejemplo `transform: rotateX(45deg);`.

  - **rotateY:** Rota el elemento a determinada cantidad de grados sobre el eje Y. Ejemplo `transform: rotateY(45deg);`.

  - **rotateZ:** Rota el elemento a determinada cantidad de grados sobre el eje Z. Ejemplo `transform: rotateZ(45deg);`.

  - **scale:** Incrementa o decrementa el tamaño del elemento de acuerdo con la proporción dada en los parámetros para el ancho y el alto. Ejemplo `transform: scale(2, 3);` incrementa el tamaño del elemento dos veces su ancho y 3 veces su alto; `transform: scale(0.5, 0.5);` decrementa el tamaño del elemento la mitad de su ancho y la mitad de su alto. Este método se acompaña de 2 métodos extra `scaleX` y `scaleY` los cuales permiten incrementar o decrementar el ancho o el alto respectivamente de manera individual.

  - **skew:** Inclina el elemento sobre el eje X o Y cierta cantidad de grados dependiendo de los parámetros dados. Ejemplo `transform: skew(20deg, 10deg);` inclina el elemento 20 grados en el eje X y 10 grados en el eje Y. Este método se acompaña de 2 métodos extra `skewX` y `skewY` los cuales permiten inclinar sobre el eje X o el eje Y respectivamente de manera individual.

  - **matrix:** Este método combina todos los anteriores en uno solo, toma 6 parámetros que corresponden a cada una de los métodos individuales de transformación en el orden `matrix(scaleX, skewY, skewX, scaleY, translateX, translateY)`. Ejemplo `transform: matrix(1, -0.3, 0, 1, 0, 0);` el ancho del elemento se queda igual, ya que la escala es 1; pero lo inclina negativamente 0.3 grados sobre el eje Y, sin inclinarlo sobre el eje X y manteniendo la misma altura ya que la escala es 1, sin moverlo sobre el eje X ni sobre el eje Y. Se usa más para minimizar código.

Ejemplo:
/* Mueve el elemento 50 píxeles a la derecha y 100 píxeles hacia abajo */

```css
.mover-elemento {
 transform: translate(50px, 100px);
}

/* Rota el elemento 45 grados */
.rotar-elemento-positivo {
 transform: rotate(45deg);
}

/* Rota el elemento -45 grados */
.rotar-elemento-negativo {
 transform: rotate(-45deg);
}

/* Incrementa el elemento dos veces su ancho y 3 veces su alto */
.incrementar-elemento {
 transform: scale(2, 3);
}

/* Decrementa el elemento la mitad de su ancho y alto */
.disminuir-elemento {
 transform: scale(0.5, 0.5);
}

/* Inclina el elemento 20 grados en el eje X y 10 grados en el eje Y */
.inclinar-elemento {
 transform: skew(20deg, 10deg);
}

/* Transforma el elemento con el shortcut `matrix` */
.transformar-elemento {
 /* matrix(scaleX, skewY, skewX, scaleY, translateX, translateY) */
 transform: matrix(1, -0.3, 0, 1, 0, 0);
}

/* Rota el elemento en los grados dados para cada eje */
.rotar-elemento-3D {
 transform: rotateX(150deg);
 transform: rotateY(130deg);
 transform: rotateZ(90deg);
}
```

# Transiciones

Además de las transformaciones matemáticas que habilita CSS, éste también ofrece otros métodos matemáticos para realizar cambios en los valores de las propiedades de un elemento de manera gradual, de tal manera que se pueda observar visualmente el cambio. Para poder crear una transición, se requieren dos cosas: La propiedad CSS sobre la cual aplicar el cambio y la duración del efecto (ejemplo: `transition: width 2s;`, se le va a aplicar el ancho especificado al elemento en una transición que dure dos segundos), si no se especifica una duración, el valor default es cero, por lo que no ocurre ninguna transición, así mismo la transición es aplicada hasta el momento en el que el cambio de tamaño ocurre.

Las transiciones pueden tener distintos efectos, de tal manera que visualmente se note una distinta transición en cada elemento, para lo cual se ocupa la propiedad `transition-timing-function`, la cual permite 6 posibles valores:

  **1.	ease:** Es el valor predeterminado, específica que la transición empiece lenta, luego rápida y finalice lenta.

  **2.	linear:** Especifica que la transición tenga una misma velocidad de inicio a fin.

  **3.	ease-in:** Especifica una transición con un inicio lento.

  **4.	ease-out:** Especifica una transición con un fin lento.

  **5.	ease-in-out:** Especifica una transición con un inicio y fin lentos.

  **6.	cubic-beizer:** Permite especificar la curva de velocidad de la transición por medio de una función `cubic-beizer `, la cual recibe 4 parámetros (x1, y1, x2, y2) que corresponden a los dos puntos coordenados de la curva (inicial y final entre 0 y 1) con los cuales calcular la velocidad de la transición. Ejemplo: `transition-timing-function: cubic-beizer(0.75, 0.56, 0.19, 0.67);`.

También es posible especificar un retraso en la aplicación de la transición, usando la propiedad `transition-delay` la cual recibe un valor en segundos que especifica el tiempo de retraso antes de que comience la transición.

Se pueden especificar dos o más propiedades y aplicarles una transición, incluso se puede hasta aplicar transiciones a transformaciones (ejemplo: `transition: width 2s, height 4s, transform 2s;`).

También acepta los valores del efecto directamente, de tal manera que todo se pueda especificar en una misma propiedad de ésta manera `transition: <transición> <efecto> <retraso>;` (ejemplo `transition: width 2s linear 1s;`).

Ejemplo:
```css
/* Transición sobre todos los divs del documento HTML */
div {
 width: 500px;
 height: 100px;
 background: gray;
 transition: width 2s;
}

/* Cambia el tamaño del div cuando se pasa el ratón sobre éste */
div:hover {
 width: 800px;
}

.transicion-linear {
 transition-timing-function: linear;
}

.transicion-ease {
 transition-timing-function: ease;
}

.transicion-ease-in {
 transition-timing-function: ease-in;
}

.transicion-ease-out {
 transition-timing-function: ease-out;
}

transicion-ease-in-out {
 transition-timing-function: ease-in-out;
}

/* Transición asignada con propiedades separadas */
.transicion-separada {
 transition-property: width;
 transition-duration: 2s;
 transition-timing-function: linear;
 transition-delay: 1s;
}

/* Transición asignada en una misma propiedad */
.transicion-completa {
 transition: width 2s linear 1s;
}
```
**_Ejemplo transiciones en CSS_**


>#### Hola, espero que lo que te mostré anteriormente te haya sido fácil de comprender. También es importante que puedas tomar un descanso, recuerda que nuestro cuerpo y nuestra mente necesitan un respiro, por lo que te invito a ver el [siguiente video](https://www.youtube.com/watch?v=tA2kT8eSjtg) y luego de que hagas esos ejercicios podrás continuar con tu lectura.
>#### Seguimos...


# Git: Sistema de Control de Versiones

Git es una herramienta para el control de versiones.

Se encarga de llevar un registro de cada cambio hecho al código, por lo que el trabajo en equipo (remoto y presencial) se desenvuelve de una manera natural. 

Este sistema es distribuido, gratuito y de código abierto, el cual fue diseñado para manejar desde proyectos pequeños hasta ser usado en proyectos de gran envergadura sin sacrificar velocidad ni eficiencia, y a su vez siendo fácil de aprender.

En el 2005 Linus Torvalds, el creador del sistema operativo Linux, decidió crear su propia herramienta para mejorar el proceso de desarrollo del kernel de Linux y desde ese momento se volvió indispensable en el día a día de los desarrolladores, de tal manera que este sistema de control de versiones distribuido ha resultado de mucha ayuda en todos los ámbitos del desarrollo de software, ya que habilita el acceso entero al código base de cualquier aplicación, lo que permite un fácil acceso a bifurcaciones y fusiones de código.

Un proyecto normalmente se guarda en un servidor git de manera remota, al cual todos los miembros del equipo de desarrollo deben tener acceso. Al proyecto almacenado remotamente se le llama repositorio de código  y el uso de git permitirá manejar correctamente los cambios y rastrear todos y cada uno de ellos.

[Presiona aquí para descargar una infografía, relacionada con el concepto anterior](https://github.com/U-Camp/BOOT-M1-SEM2/blob/main/infografia/S1_Infograf%C3%ADa%203_2.pdf)

Para usar Git son suficientes unos cuantos comandos, por ejemplo, para inicializar git y que el proyecto en el que estemos trabajando empiece a ser rastreado, basta con escribir en la terminal dentro de la carpeta del proyecto que se quiera empezar a rastrear:

`$ git init`

Normalmente este comando se usa una sola vez por proyecto.

Cuando se requiere descargar un proyecto ya existente en algún servidor externo, es posible hacer eso con el comando:

`$ git clone <ruta_proyecto_en_servidor_git>`

Finalmente, si se ocupa realizar una sincronización del código local con el código del servidor remoto, se necesita ejecutar el comando:

`$ git pull origin <rama_remota>`

El término **origin** normalmente hace referencia a la URL del servidor git remoto; este comando obtiene los últimos cambios de la rama remota (normalmente master o develop) y los mezcla automáticamente con la rama de trabajo actual.

## Agregar cambios

Cuando estamos trabajando cambios en `git`, una vez inicializada la carpeta con `git init`, es importante prepararlos para que se guarden en el historial de cambios.

Para realizar un proceso de preparación se utiliza, dentro de la terminal:

`git add .`

Esto permite guardar los cambios en un estado de preparación. Es decir, aún nos falta confirmarlos. Sin embargo, si realizas este comando podrás ver los cambios que están por ejecutarse:

`git status`


## Confirmar cambios

Una vez que tenemos un conjunto de cambios preparados para confirmarse dentro del historial de cambios, lo que haremos es aplicar el siguiente comando:

`git commit -m "MENSAJE"`

Es importante establecer el argumento `-m` para poder generar el mensaje involucrado describiendo los cambios que hiciste en doble comillado.

Resumiendo, cada vez que necesites guardar cambios en el historial de cambios del proyecto, deberás utilizar:

- `git add`
- `git commit -m "___"`

## Ramas

En ocasiones, cuando se realizan mezclas entre ramas (`git pull origin <rama_remota> `), es posible encontrarse con diferencias que el sistema de control de versiones no puede resolver automáticamente, por lo que se hace necesario resolverlas manualmente, cuando esto sucede git informa aquellos archivos afectados por un conflicto y se procede a resolver esos conflictos manualmente, validando los cambios locales con los remotos en cada uno de los archivos modificados y mezclando, también manualmente, estos cambios, de tal manera que los archivos afectados queden en una versión estable y validada sin que ningún cambio se pierda, por lo que se requiere a su vez de un `git commit` de la mezcla haciendo uso de `git merge` o `git rebase` para confirmar la resolución de los conflictos.

Para generar una nueva rama en base a alguna rama base, se puede usar: 

`$ git checkout <rama_base>`

Para moverse y crear una rama en la cual se quiera empezar a trabajar se usa el comando:

`$ git checkout -b <nombre_nueva_rama>`

>#### Si deseas consultar y descargar una infografía que explica un poco lo anterior, [presiona aquí](https://github.com/U-Camp/BOOT-M1-SEM2/blob/main/infografia/M1_S3_Infograf%C3%ADa%201_2.pdf)
>
>#### El siguiente contenido va relacionado con GitHub que es la plataforma en donde estás viendo este contenido, tiene muchas funciones que en tu campo laboral podrás utilizar y te serán de gran ayuda, seguimos adelante...


# GitHub: Plataforma para colaboración de software

GitHub es una plataforma que nos permite colaborar con profesionales de desarrollo y como te comenté es la plataforma que actualmente estás utilizando para leer este contenido.

Encuentra el sitio en: www.github.com

Una vez que accedes, registrarás una cuenta y, posteriormente, podrás explorar los diferentes proyectos abiertos que existen por comunidades, organizaciones e incluso conectar con más personas.

Es importante considerar que tan pronto tienes creada una cuenta, puedes crear un repositorio en tu perfil. Los repositorios son los diferentes proyectos (que representan historiales de cambios) guardados en los servidores de GitHub.

Las ventajas de tener tus proyectos en GitHub, es permitir a otras personas descargar o clonar estos repositorios para probarlos por su cuenta.

Para que puedas subir un proyecto a un repositorio, tendrás que seguir estos pasos:

- Crear un repositorio nuevo dentro de tu cuenta de GitHub.
- Obtendrás la dirección `.git` del repositorio, entregada al momento. La copiarás y la guardarás un momento.
- Abrirás Visual Studio Code.
- Crearás una carpeta `demo-git` y dentro, harás un archivo `index.html`.
- Dentro de Visual Studio Code, abre la carpeta de `demo-git`.
- Abre la terminal, que se encuentra en la parte superior, en el navegador del programa. 
- Dentro de la terminal, escribe la inicialización de:

```shell
git init
```

- Una vez hecho esto, ejecuta un proceso básico de guardado de cambios:

```shell
git add -A
git commit -m "Primer ejemplo"
```

- Posteriormente, ejecutarás este comando:

`git remote add origin REPO_URL`

Ahora, `REPO_URL` lo sustituirás por la dirección `.git` que copiamos. Sería un ejemplo similar a esto:

`git remote add origin https://github.com/*********.git`

- Una vez realizada la conexión remota, es momento de empujar nuestros cambios desde nuestra área local a una área remota. Esto lo haremos con:

`git push origin master`

Con esto, subirán los cambios. Cabe destacar que `master` significa la rama en la cual nosotros queremos subir nuestros cambios. El repositorio de GitHub deberá ser similar al del área local constantemente para mantenernos actualizados.

- Terminado esto, podremos recargar la página y ver nuestro proyecto en la plataforma de GitHub.

> #### No olvides esta información, ya que, uno de los criterios que se te estaría evaluando en la entrega de tus proyectos esta relacionado a la documentación misma en GitHub.
> #### Llegaste al final del contenido correspondiente a la semana 2, recuerda repasar cada vez que sea necesario y prestar mucha atención a las U Class. También te recuerdo que puedes hacer las preguntas que consideres a tus coaches desde Teams. 
> #### Saludos  :blush:

