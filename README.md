![Banner](imagenes/banner.png)

# M1S2: Git y GitHub.

> #### ¡Hola!👋🏻🤖 ¿Qué tal? ¿Cómo te sientes? ¿Qué te ha parecido el contenido que has aprendido hasta el día de hoy?🤗
> #### Recuerda que si tienes alguna duda, cuentas con los foros de discusión en Microsoft Teams para que escribas tus dudas y entre tus compañeros puedan ayudarte a disiparlas.
> #### A continuación, seguimos con el contenido correspondiente a este módulo, en donde conoceremos Git, los comandos básicos más comunes que debes de conocer de este controlador de versiones y su flujo de trabajo. Además, daremos un repaso breve por GitHub y haremos nuestro primer repositorio.🤩💻
> #### Iniciemos…


## **ÍNDICE**

* [Introducción a Git: Sistema de Control de Versiones](https://github.com/U-Camp/BOOT-M1-SEM2-WDF#introducci%C3%B3n-a-git-sistema-de-control-de-versiones)
  * [Comandos Básicos de Git](https://github.com/U-Camp/BOOT-M1-SEM2-WDF#comandos-b%C3%A1sicos-de-git)
   * [Agregar Cambios](https://github.com/U-Camp/BOOT-M1-SEM2-WDF#agregar-cambios) 
   * [Confirmar Cambios](https://github.com/U-Camp/BOOT-M1-SEM2-WDF#confirmar-cambios) 
* [Introducción a GitHub: Plataforma para Colaboración de Software](https://github.com/U-Camp/BOOT-M1-SEM2-WDF#introducci%C3%B3n-a-github-plataforma-para-colaboraci%C3%B3n-de-software)


# Introducción a Git: Sistema de Control de Versiones

Git es una herramienta para el control de versiones.

Se encarga de llevar un registro de cada cambio hecho al código, por lo que el trabajo en equipo (remoto y presencial) se desenvuelve de una manera natural. 

Este sistema es distribuido, gratuito y de código abierto, el cual fue diseñado para manejar desde proyectos pequeños hasta ser usado en proyectos de gran envergadura sin sacrificar velocidad ni eficiencia, y a su vez siendo fácil de aprender.

En el 2005 Linus Torvalds, el creador del sistema operativo Linux, decidió crear su propia herramienta para mejorar el proceso de desarrollo del kernel de Linux y desde ese momento se volvió indispensable en el día a día de los desarrolladores, de tal manera que este sistema de control de versiones distribuido ha resultado de mucha ayuda en todos los ámbitos del desarrollo de software, ya que habilita el acceso entero al código base de cualquier aplicación, lo que permite un fácil acceso a bifurcaciones y fusiones de código.

Un proyecto normalmente se guarda en un servidor git de manera remota, al cual todos los miembros del equipo de desarrollo deben tener acceso. Al proyecto almacenado remotamente se le llama repositorio de código  y el uso de git permitirá manejar correctamente los cambios y rastrear todos y cada uno de ellos.

[Presiona aquí para descargar una infografía, relacionada con el concepto anterior](https://github.com/U-Camp/BOOT-M1-SEM2/blob/main/infografia/S1_Infograf%C3%ADa%203_2.pdf)

## Comandos Básicos de Git
Para usar Git son suficientes unos cuantos comandos, por ejemplo, para inicializar git y que el proyecto en el que estemos trabajando empiece a ser rastreado, basta con escribir en la terminal dentro de la carpeta del proyecto que se quiera empezar a rastrear:

`$ git init`

Normalmente este comando se usa una sola vez por proyecto.

Cuando se requiere descargar un proyecto ya existente en algún servidor externo, es posible hacer eso con el comando:

`$ git clone <ruta_proyecto_en_servidor_git>`

Finalmente, si se ocupa realizar una sincronización del código local con el código del servidor remoto, se necesita ejecutar el comando:

`$ git pull origin <rama_remota>`

El término **origin** normalmente hace referencia a la URL del servidor git remoto; este comando obtiene los últimos cambios de la rama remota (normalmente master o develop) y los mezcla automáticamente con la rama de trabajo actual.

## Agregar Cambios

Cuando estamos trabajando cambios en `git`, una vez inicializada la carpeta con `git init`, es importante prepararlos para que se guarden en el historial de cambios.

Para realizar un proceso de preparación se utiliza, dentro de la terminal:

`git add .`

Esto permite guardar los cambios en un estado de preparación. Es decir, aún nos falta confirmarlos. Sin embargo, si realizas este comando podrás ver los cambios que están por ejecutarse:

`git status`


## Confirmar Cambios

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


# Introducción a GitHub: Plataforma para Colaboración de Software

GitHub es una plataforma que nos permite colaborar con profesionales de desarrollo y como te comenté es la plataforma que actualmente estás utilizando para leer este contenido.

Encuentra el sitio oficial en: www.github.com

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

> #### Llegaste al final del contenido correspondiente a este módulo, recuerda repasar cada vez que sea necesario y prestar mucha atención a todo el contenido que tienes en  Microsoft Community Training. 
> #### ¡Saludos!  :blush:

