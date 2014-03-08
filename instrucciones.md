Instalar git

    sudo apt-get install git-core

Comprobar la versión

    git --version

Configurar nuestro usuario

    git config --global user.name "Fer Perales"
    git config --global user.email me@ferperales.net

Otras preferencias

    git config --global core.editor gvim
    git config --global core.mergetool vimdiff
    git config --global color.ui true


Inicializando un repo

    git init

Creando un archivo de prueba

    touch README.md

Verificar el estatus

    git status

Trackear el nuevo archivo

    git add README.md

Crear un archivo .gitignore

    touch .gitignore

Ver la diferencia entre cambios

    git diff

Ver diferencia incluyendo stage

    git diff --cached

Primer commit

    git commit

Commit saltando el área de stage

    git commit -a -m "Primer commit"


Borrando archivos

    rm test.dm

¿Qué pasó?

    git rm test.dm


Ver el log

    git log

Un mejor log

    git log --prety=oneline

log con gui

    gitk

Algo que olvidé

    git commit --amend

Quitar del stage

    git reset HEAD file.md

Deshaciendo cambios

    git checkout -- file.md

----------------

Clonando un repo

    git clone git@github.com:ferperales/git-fundamentals-workshop

Viendo los remotos

    git remote -v

Agregando un remoto

    git remote add remotename git@github.com:tunombre/turepo

Actualizando desde el remoto

    git fetch

Empujando a mi remoto

    git push origin master

Actualizando mi remoto y rama actual

    git pull origin master

----------------

Creando una nueva rama

    git checkout -b 'nueva_rama'

Ya que terminé, regreso a master

    git checkout master

Y mergeo mi rama

    git merge nueva_rama

Ver mis ramas

    git branch

Ver ramas mergeadas a mi actual

    git branch --merged

Borrar ramas

    git branch -d rama

Si ya fue mergeada, lo hará sin problemas pero, sino lo ha sido, podemos
forzarlo

    git branch -D rama_no_mergeada
