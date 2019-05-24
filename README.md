# Bootstrap-template
Steps to create a Bootstrap template with the task runner called Gulp with the help of the Node.js development environment

## 1) INITIALIZATION
### To initialize a project in Node.Js:

```bash
npm init --yes
```

### This will create the file "package.json" with the Project Description. EJ:

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

## 2) INSTALL THE DEPENDENCIES

* Bootstrap (The Css Framework)
* Jquery (We download it because Bootstrap uses it to add more animations)
* Popper.js (Jquery makes use of this for modal windows, alerts, acoordions, etc.)
* Font-Awesome (From this we get the Icons)

```bash
	npm install bootstrap font-awesome jquery popper.js
```
### This will update the file "package.json" and it would look like this:

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
### A directory with the name "node_modules" with the following directories will also be created inside:

* bootstrap 
* font-awesome 
* jquery 
* popper.js 

<hr>

## 3) INSTALL THE TOOLS THAT WILL HELP US IN DEVELOPMENT

* Gulp (A Task Runner)
* Gulp tools (Gulp functions that help us execute Tasks Automatically)
* Browser-sync (Generator of a server, this will help us that every time we save the project the browser will refresh)

```bash
    npm install -D gulp gulp-cli gulp-sass browser-sync
```
As we can see after <b> "install" </ b> add <b> "- D" </ b> this is so that we do not install these tools as dependencies,
since our project will not depend on these, because they will only help us in the development.
The file <b> "package.json" </ b> will be updated and would look like this:

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

## 4) WE CREATE OUR WORK ARCHIVES

* We create the file <b> "gulpfile.js" </ b>: In this file we will write all the tasks automated with Gulp.
* We created the following route <b> "src / scss / main.scss" </ b>: Here all the Sass code that we will write will go.
* We create the HTML file in the following directory <b> "src / index.hmtl" </ b>: In this way we are creating all the necessary HTML files

<hr>

## 5) WE PROGRAM THE TASKS

### In the file "gulpfile.js" we program the tasks that we want to automate.

<hr>

## 6) WE CREATE OUR PERSONALIZED COMMAND FROM THE ENVIRONMENT OF NODE.JS

### In the "package.json" file, within the "scripts" value we add:

```json
    "scripts": {
    "start": "gulp"
    }
```

### We would stay as follows:

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

## 7) WE EXECUTE THE PERSONALIZED COMMAND THAT WAS CREATED

 Executing the following command will be the same as executing the "gulp" command:

```bash
    npm start
```

