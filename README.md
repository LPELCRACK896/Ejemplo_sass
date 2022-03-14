# Ejemplo SASS

## Utilizar compilador SASS con npm 
### Primero inicializamos el proyecto npm
```
npm init
```
### Instalamos el compilador
```
npm i node-sass --save-dev
```

### Modificamos el archivo _package.json_
Al json valor de scripts le agregamos una llave llamada _compiler:sass_ 

#### Originalmente viene asi: 
- scripts: {}
#### Luego de realizar cambios debe verse así
-scripts: {"compiler:sass"}

No importa si hay otros scripts, solo lo añadimos al json valor. 

Al _compiler:sass_, le ponemos como valor "node-sass {direccion_del_archivo_sass_origen} {direccion_del_archivo_css_destino}"

En este proyecto quedo así: 
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
    ,"compiler:sass": "node-sass src/sass/main.scss src/css/main.css"
  s