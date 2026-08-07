# primer flujo con Git

## Objetivo 

Crear un repositorio Git y sincronizarlo con GitHub

## Paso 1.  Terminal/bash

pwd = Mostrar la carpeta actual
/c/Users/larau

## Paso 2.

Crear la carpeta ERP-Software-Architecture
mkdir ERP-Software-Architecture

## paso 3.

Ingrsar a la carpeta ERP-Software-Architecture
cd  ERP-Software-Architecture

## Paso 4.

Confirmar en que carpeta estoy
pwd
/c/Users/larau/ERP-Software-Architecture

## Paso 5.

Convertir la carpeta en un repositorio Git creando la carpeta oculta .git
git init
Initialized empty Git repository in C:/Users/larau/ERP-Software-Architecture/.git/

La carpta .git esta oculta pero es el cerebro del repositorio ahi guarda: historial de cambios, ramas, commits, etiquetas, configuración del repositorio etc.

## Paso 6.

Consultar cambios o el estado del repositorio local
git status = 
On branch main 

No commits yet 

nothing to commit (create/copy files and use "git add" to track)

On branch main "Significa: Actualmente estás trabajando en la rama main."
No commits yet "Significa: Todavía no has guardado ninguna versión del proyecto."
nothing to commit "Significa:No hay archivos nuevos o modificados para guardar."


## Paso 7.

Crear la carpeta docs y la images dentro de (main)
primero mkdir docs "enter", luego  mkdir docs/images "enter"
Otra opcion más rapida crear las dos carpetas de una vez mkdir -p docs/images "enter"
-p significa que, si docs no existe, Git Bash la crea automáticamente y luego crea images dentro de ella. 

## Paso 8.

Visualizar lista de archivos y carpetas
ls =
docs/

## Paso 9.

Visualiar lista de archivos o carpetas dentro de docs
ls docs =
images/

## Paso 10.

Rectificar en que carpeta estamos o ubicacion actual
pwd
/c/Users/larau/ERP-Software-Architecture

# Observación

Usando Git bash no usamos slash invertido para construir una ruta como en CMD, se usa el slash /


## Paso 10.

Buscar carpeta o archivo que deseamos copiar para luego pegar en nuestra carpeta docs
ls /c/Users/larau/OneDrive/Documents 

Acá visualizamos los archivos o carpetas que esrtan dentro de Documents

 arc42-template-ES-withhelp-markdown/  'Borrador Normas Aps.docx'     desktop.ini  'Plantillas personalizadas de Office'/   PowerShell/   WindowsPowerShell/
'Bloc de notas de OneNote'/             CWindowssystem32cmd.exe.txt   LUIS/         PlantUML/                               UMB/

## Paso 11. 

Visualizar el contenido de la carpeta arc42-template-ES-withhelp-markdown

ls /c/Users/larau/OneDrive/Documents/arc42-template-ES-withhelp-markdown = 
arc42-template-ES.md  images/

## Paso 12.

Copiar el archivo Markdown a mi proyecto 
cp /c/Users/larau/OneDrive/Documents/arc42-template-ES-withhelp-markdown/arc42-template-ES.md docs/

## Paso 13. 

Copiar la carpeta images, pero aquí usé * porque ya creamos la carpeta docs/images. Así solo copiamos el contenido de images y no creamos una carpeta images dentro de otra images.

cp -r /c/Users/larau/OneDrive/Documents/arc42-template-ES-withhelp-markdown/images/* docs/images/


## Paso 14.

Veirificar la lista de archivos o carpetas copiados del paso 13

ls docs = 
arc42-template-ES.md  images/

## Paso 15.

Verificar la lista de archivos o carpetas dentro de images

ls docs/images = 
05_building_blocks-ES.png  10_stimulus.png  arc42-logo.png

## Paso 16.

Consultar cambios o el estado del repositorio local
git status = 
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        docs/

nothing added to commit but untracked files present (use "git add" to track)

# Observación 

A diferencia del paso 6 ahora el git status nos muestra Untracked "Significa: Veo que agregaste archivos nuevos, pero todavía no forman parte del historial del proyecto." 

## Paso 17.

Le indicamos a Git que queremos guardar todo
git add .
warning: in the working copy of 'docs/arc42-template-ES.md', LF will be replaced by CRLF the next time Git touches it

## Paso 18.

Consultamos nuevamente los cambios o el estado del repositorio local
git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   docs/arc42-template-ES.md
        new file:   docs/images/05_building_blocks-ES.png
        new file:   docs/images/10_stimulus.png
        new file:   docs/images/arc42-logo.png

# Observación 
Changes to be committed: Git esta diciendo Ya entendí cuáles archivos quieres guardar en la próxima versión.

## Paso 19.

Ahora le decimos que esta sera la nueva version del proyecto, esto actualiza los cambios y agreamos un comentario -m "Comentario bien especifico", nos servira para cuando deseamos volver a una version anterior entenderla rapidamente

git commit -m "Agregar estructura inicial arc42" 

[main (root-commit) 6e5f72f] Agregar estructura inicial arc42
 4 files changed, 998 insertions(+)
 create mode 100644 docs/arc42-template-ES.md
 create mode 100644 docs/images/05_building_blocks-ES.png
 create mode 100644 docs/images/10_stimulus.png
 create mode 100644 docs/images/arc42-logo.png

# Observación 
# [main]
Significa que el commit se hizo sobre la rama main.

# (root-commit)
Esta palabra aparece solo una vez en la vida de un repositorio.
Significa: Este es el primer commit del proyecto, a partir del siguiente commit ya no volvera a salir.

# 6e5f72f
Ese número es el identificador único del commit (SHA). Cada commit del mundo tiene un identificador diferente, en el futuro se puede hacer git show 6e5f72f para volver a esta versión.

# files changed
Git detectó que agregue cuatro archivos.

# 998 insertions
Git también sabe cuántas líneas nuevas ingresaron al proyecto.

## Paso 20.

Vuelvo a vaalidar los cambios o el estado del repositorio local
git status
On branch main
nothing to commit, working tree clean

# Observación
Ahora me sale esto nothing to commit, working tree clean: Significa todo está guardado. No hay cambios pendientes.

## Paso 21.

Para conectar el repositorio de GitHub a nuestro proyecto Git y poderlo publicar entramos a GitHub, visualizamos <> Code y al dar clic aparecerá una dirección parecida a esta
https://github.com/Laraujo-hub/ERP-Software-Architecture.git

Copiamos esa dirección 

## Paso 22.

Ahora ejecutamos git remote add origin y agregamos la url copiada
git remote add origin https://github.com/Laraujo-hub/erp-software-architecture.git

## Paso 23. 

Ahora verificamos que si quedo configurada debemo ver dos Origin uno con fetch y otro push
git remote -v
origin  https://github.com/Laraujo-hub/erp-software-architecture.git (fetch)
origin  https://github.com/Laraujo-hub/erp-software-architecture.git (push)

# Observación

cuando usamos Origin le indicamos a Git Mi repositorio remoto principal se llama origin.
fetch → Traer cambios desde GitHub hacia tu computador.
push → Enviar cambios desde tu computador hacia GitHub.

## Paso 24. 

Por ser la primera ves que creamos la conexion remota a nuestro repositorio usamos -u origin main
git push -u origin main

info: please complete authentication in your browser...
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 16 threads
Compressing objects: 100% (7/7), done.
Writing objects: 100% (8/8), 311.57 KiB | 18.33 MiB/s, done.
Total 8 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Laraujo-hub/erp-software-architecture.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.

# Observación 
git push → Enviar cambios.
origin → Al repositorio remoto que acabo de configurar.
main → La rama que voy publicar.
-u (--set-upstream) → Le dice a Git:
"Recuerda que mi rama local main está asociada con origin/main."

Pero a partir del segundo commit solo usamos: git push y Git ya sabrá a dónde enviar los cambios.

El resultadoo significa que nuestro repositorio local y GitHub ya están sincronizados.

# FIn Repositorio Sincronizados

---------------------------------------------------------------------------------------------

larau@LARAUJO MINGW64 ~/ERP-Software-Architecture (main)
$ pwd
/c/Users/larau/ERP-Software-Architecture

larau@LARAUJO MINGW64 ~/ERP-Software-Architecture (main)
$ mkdir docs/git

# Crear un archivo Markdown vacio con el objetico de comentar como Crear un repositorio Git y sincronizarlo con GitHub

larau@LARAUJO MINGW64 ~/ERP-Software-Architecture (main)
touch docs/git/01-primer-flujo-git.md

# Abrir la carpeta o arcihvo en la cual estoy ubicado actualmente 

larau@LARAUJO MINGW64 ~/ERP-Software-Architecture (main)
$ code .

 