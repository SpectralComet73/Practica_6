Carlos Alexis Rendon Sierra

## a.      ¿Cómo se inicializa un repositorio en Git?

Para inicializar un repositorio en git basta con ejecutar el comando ```git init``` en la terminal.
Esto quedaria de la siguiente manera:
```bash
git init
```

## b.      ¿Cómo creas un repositorio en GitHub?

Para crear un repositorio en GitHub, lo primero sería tener una cuenta en GitHub y, por supuesto, tener iniciada la sesión. Después, buscar la opción de crear nuevo repositorio, ya sea en alguna sección del menu home o en la sección de repositorios a la que se puede acceder dando click en nuestro perfil. Una vez ahí deberemos llenar el campo de nombre para el repositorio, así como una descripción opcional y seleccionar si queremos que sea público o privado. También existen opciones como añadir un archivo README.md o un archivo gitignore y licencia, pero no son obligatorios. Una vez llenados los campos, deberemos dar clic en el botón de crear repositorio.

## c.      ¿Cómo vinculas un repositorio local de Git con uno remoto en GitHub?

Para ello, primero tenemos que tener nuestro repositorio local de git creado e inicializado, además de tener creado el repositorio en GitHub al cual queremos vincular nuestro repositorio local. Una vez hecho esto, debemos copiar la URL del repositorio de GitHub al que queremos vincular el repositorio local. Esto lo haremos mediante el siguiente comando.
```bash
git remote add origin https://github.com/usuario/repositorio.git
```
La URL la podemos obtener en donde dice <>Code en nuestro repositorio de GitHub.

## d.      ¿Cuál es el flujo básico de trabajo en Git y GitHub?

El flujo básico de trabajo en Git y GitHub, bajo la suposición de que ya tenemos un repositorio local y uno remoto vinculados, consistiría en realizar cambios en el repositorio local y posteriormente subirlos al repositorio remoto. Para ello, primero deberemos agregar los cambios al área de preparación con el comando
```bash
git add .
``` 
Donde el punto indica que se agregarán todos los cambios, ya que si queremos agregar solo un archivo en específico, deberemos poner el nombre del archivo en lugar del punto.

Posteriormente, hacer un commit con el comando

```bash
 git commit -m "mensaje"
```
Donde el mensaje es una breve descripción de los cambios realizados.

Una vez hecho esto, podremos subir los cambios al repositorio remoto con el comando 
```bash
git push origin main
```
Esto es, si es la primera vez, subimos cambios; de lo contrario, basta con ejecutar el comando 
```bash
git push
``` 
(Tener en cuenta que en lugar de main puede ser el nombre de la rama en la que estemos trabajando)

## e.      ¿Para qué sirve el archivo .gitignore?

Permite indicarle a git que archivos no queremos que se suban para que no sean tomados en cuenta a la hora de hacer un commit.

## f.       ¿Cuál es el propósito de una rama?

Nos permite trabajar en diferentes versiones de un mismo proyecto sin alterar al proyecto principal que vendría siendo la rama principal o main.

Se crea con el comando 
```bash
git branch nombre_rama
```
Y se cambia a la rama con el comando 
```bash
git checkout nombre_rama
```
Si queremos eliminar una rama, debemos estar en otra rama y ejecutar el comando 
```bash
git branch -d nombre_rama
```

## g.      ¿Qué es una fusión?

Es la acción de unir dos ramas en una sola.

Se realiza con el comando 
```bash
git merge rama_secundaria
```
Esto debe hacerse estando en la rama principal o la que queremos que quedara con la fusión.

## h.      Explica los diferentes tipos de fusión que existen.

Existen dos tipos de fusiones: la fusión fast forward y la fusión manual. En la fusión fast forward la fusión se realiza automáticamente sin ningún problema, ya que no existen conflictos entre las ramas, mientras que en la manual se deben resolver los conflictos que existan entre las ramas antes de realizar la fusión.

## i.       ¿Cómo puedes ver el historial de tu repositorio?

Con el comando 
```bash
git log
```
Esto nos mostrará todo el historial de commits realizados en el repositorio.

Una forma más cómoda de verlo sería con el comando
```bash
git log --oneline
```
Esto nos mostrará el historial de commits en una sola línea.

## j.       ¿Cuál es el propósito de una etiqueta?

Nos permite versionar nuestro proyecto, esto ya que marca un punto en el historial de nuestro repositorio.

Se crea con el comando 
```bash
git tag nombre_etiqueta
```
Luego, para que se vea reflejada en el repositorio remoto, debemos hacer un commit y posteriormente ejecutar el comando 
```bash
git push origin nombre_etiqueta
```


