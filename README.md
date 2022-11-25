# Práctica del curso de git, gitHub y Sourcetree 

### KeepCoding Bootcamp - Web / Enrique Pina Navarro

## Ejercicio 1 

- ¿Qué comando utilizaste en el paso 11? ¿Por qué?  
    `$ git reset --hard HEAD~1` \
    Porque `git reset` deshace un comit, el `--hard` pierde los cambios realizados en el *working copy* (como si después del `git reset` realizo un `git restore`) y el `HEAD~1` indica un commit anterior (podemos volver varios commits a tras indicando el número.)   

- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué? \
    `$ git reflog` \
    Para ver el historial por donde he pasado y conseguir el código del commit al que quiero volver.

    `$ git reset 847a62f` \
    `$ git commit -m “mensaje commit"` \
    Con `git reset` vuelvo al commit que le indico con el código, pero tengo que guardar los cambios porque es lo que tenía  en este commit.

- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué? \
    `$ git merge master` \
    No causo conflicto porque la rama absorbida *master* está  en un commit anterior de grafo.

- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?  
    `$ git checkout styled`\
    Para cambiar a la rama *styled*. 

    `$ git merge htmlife`\
    Para hacer el *merge*.\

    Si causó conflicto, porque el archivo *git-nuestro.md* es diferente en el mismo punto. En la rama *styled* tenemos marcado el archivo con `"*"`  y en la *htmlife* (que hemos creado desde master y master estaba un commit atrás del cambio), está  moficado con lenguaje `“html”`

- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?\
    `$ git checkout master`\
    Para cambiar a la rama *master*.

    `$ git merge styled`\
    Para hacer el *merge*. 

    No causó ningún conflicto, como no existe ninguna bifurcación en el grafo entre la rama *master* y la rama *styled*, simplemente la rama *styled* tiene más commits, al realizar un *range* la ram master se sitúa en el commit de la rama *styled (Fast-forward)*

 - ¿Qué comando o comandos utilizaste en el paso 25?\
    `$ git log –graph`

 - El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?\  
    `$ git merge --no-ff title` \
    Si, porque la rama *master* está  un commit anterior a la rama *title*, por lo que *master* actualiza su posición situándose en el commit *title* y sin la necesidad de crear un commit nuevo para unir los commits que tiene *title*.

- ¿Qué comando o comandos utilizaste en el paso 27? \
    `$ git reset HEAD~1`

- ¿Qué comando o comandos utilizaste en el paso 28?\
    `$ git restore git-nuestro.md`
 
- ¿Qué comando o comandos utilizaste en el paso 29?\
    `$ git branch -D title`

 - ¿Qué comando o comandos utilizaste en el paso 30?\
    No puedo rehacer el *merge* porque la rama *title* está  borrada.

- ¿Qué comando o comandos usaste en el paso 32? \
    `$ git reflog ` \
    Para ver el código del primer commit o con un `git log` también veríamos  el código del primer commit.

    `$ git reset 9109e35`\
    Para volver al primer commit.

- ¿Qué comando o comandos usaste en el punto 33?\
    `$ git reflog ` \
    Para ver el código del commit donde puse el título.

    `$ git reset e9d88c7`\
    Para moverme a ese commit.
