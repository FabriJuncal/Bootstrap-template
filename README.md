# Bootstrap-template
Steps to create a Bootstrap template with the task runner called Gulp with the help of the Node.js development environment

## 1) INICIALIZACION
### Para Inicializar un proyecto en Node.Js:

```bash
npm init --yes
```

### Esto nos creará el archivo "package.json" con la Descripcion del Proyecto. EJ:

```json
{
  "name": "Bootstrap-template",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "",
  "license": "ISC"
}
```
<hr>

## 2) INSTALAMOS LAS DEPENDENCIAS

* Bootstrap (El Framework de Css)
* Jquery (Lo descargamos por que Bootstrap hace uso de este para poder agregar mas Animaciones)
* Popper.js (Jquery Hace uso de este para las ventanas modales, alertas, acoordeones, etc)
* Font-Awesome (De este obtenemos los Iconos)

```bash
	npm install bootstrap font-awesome jquery popper.js
```
### Esto nos actualizara el archivo "package.json" y quedaria asi:

```json
{
  "name": "Bootstrap-template-init",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "dependencies": {
    "bootstrap": "^4.3.1",
    "font-awesome": "^4.7.0",
    "jquery": "^3.4.1",
    "popper.js": "^1.15.0"
  }
}
```
### Tambien se creará un directorio con el nombre "node_modules" con los siguientes directorios dentro:

* bootstrap 
* font-awesome 
* jquery 
* popper.js 

<hr>

## 3) INSTALAMOS LAS HERRAMIENTAS QUE NOS AYUDARÁN EN EL DESARROLLO

* Gulp ( Un Task Runner)
* Herramients de Gulp ( Funciones de Gulp que nos ayudan a ejecutar Tareas Automaticamente )
* Browser-sync ( Generador de un servidor, este nos ayudará a que cada ves que guardemos el proyecto el navegador se refresque )

```bash
    npm install -D gulp gulp-cli gulp-sass browser-sync
```
Como podemos ver despues de <b>"install"</b> agregamos <b>"-D"</b> esto es para que no nos instale estas herramientas como dependencias,
ya que nuestro proyecto no dependera de estos, por que solo nos ayudarán en el desarrollo.
El archivo <b>"package.json"</b> se actualizará y quedaria asi:

```json
    {
  "name": "Bootstrap-template-init",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "dependencies": {
    "bootstrap": "^4.3.1",
    "font-awesome": "^4.7.0",
    "jquery": "^3.4.1",
    "popper.js": "^1.15.0"
  },
  "devDependencies": {
    "browser-sync": "^2.26.5",
    "gulp": "^4.0.2",
    "gulp-cli": "^2.2.0",
    "gulp-sass": "^4.0.2"
  }
}
```
<hr>

## 4) CREAMOS NUESTROS ARCHIVOS DE TRABAJO

* Creamos el archivo <b>"gulpfile.js"</b> : En este archivo escribiremos todas las tareas automatizadas con Gulp.
* Cremos la siguiente ruta <b>"src/scss/main.scss"</b> : Aqui irán todo el codigo Sass que vayamos escribiendo.
* Creamos el archivo HTML en el siguiente directorio <b>"src/index.hmtl"</b>: De esta manera vamos creando todos los archivos HTML necesarios

<hr>

## 5) PROGRAMAMOS LAS TAREAS

### En el archivo "gulpfile.js" programamos las tareas que queremos automatizar.

<hr>

## 6) CREAMOS NUESTRO COMANDO PERSONALIZADO DESDE EL ENTORNO DE NODE.JS

### En el archivo "package.json", dentro del valor "scripts" agregamos:

```bash
    "scripts": {
    "start": "gulp"
    }
```

### Nos quedaria de la siguiente forma:

```json
{
  "name": "Bootstrap-template-init",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "start": "gulp"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "dependencies": {
    "bootstrap": "^4.3.1",
    "font-awesome": "^4.7.0",
    "jquery": "^3.4.1",
    "popper.js": "^1.15.0"
  },
  "devDependencies": {
    "browser-sync": "^2.26.5",
    "gulp": "^4.0.2",
    "gulp-cli": "^2.2.0",
    "gulp-sass": "^4.0.2"
  }
}
```
<hr>

## 7) EJECUTAMOS EL COMANDO PERSONALIZADO QUE SE CREAMOS

### Ejecutar el siguiente comando será lo mismo que ejecutar el comando "gulp":

```bash
    npm start
```
