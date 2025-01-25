# GitPractica
Repositorio para práctica de Github

**Respuestas**

- ¿Qué comando utilizaste en el paso 11? ¿Por qué?

*git reset -- hard HEAD~1* - Para deshacer los cambios en el working copy también.

- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?

*git reflog* para encontrar el ID del commit que hemos deshecho.
*git reset 619126c* Para moverme al commit que deshicimos con el puntero de la rama styled.
*git add git-nuestro.md* y *git commit*  porque me ponía “Unstaged changes after reset:M	git-nuestro.md

- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?

No. Porque main y Style tienen la misma version de git-nuestro en el primer commit.

- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?

Sí, porque la dos ramas tenían cambios distintos en el mismo archivo y en las mismas lineas de este.

- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?

No, porque main no tenia cambios posteriores a la creacion de styled en el mismo archivo. Cuando se hace merge desde main, 
git mueve el puntero de main al ultimo commit the styled y este se absorbe en main.

- ¿Qué comando o comandos utilizaste en el paso 25?

*git log --graph --decorate --pretty=oneline*

- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?

Si,podria haber sido un merge fast-forward en el que el puntero de ' main' podría haber avanzando el puntero al ultimo commit de 'title'.

- ¿Qué comando o comandos utilizaste en el paso 27?

*git reset HEAD~1*
*git log* para comprobar

- ¿Qué comando o comandos utilizaste en el paso 28?

(Hice esto:)
*nano git-nuestro.md* elimino los cambios de titulo
*git add git-nuestro.md*
*git commit -m "descarto los cambios del titulo”* commit el borrado de esos cambios.
(Pero creo que me daba la opcion de hacer esto que habria sido mas facil:)
*git checkout --git-nuesto.md* Para descartar los cambios del working copy.

- ¿Qué comando o comandos utilizaste en el paso 29?

*git branch -D title* Para el borrado de la rama ‘title’

- ¿Qué comando o comandos utilizaste en el paso 30?

Desde main, podría haber hecho el reset -- hard a d2fcb43, y se quedarían unidas sin tener que haber creado la rama title otra vez?
*git reflog* busco el id del commit del  merge de title con main,
*git reset —hard d2fcb43* Vuelvo al commit donde hice el merge de main con title descartando los cambios en el working copy. (Detached head)
*git branch title* creo la rama title otra vez.
*git checkout title* y compruebo que mi working copy contiene los cambios de title.
*git checkout main*
*git reset —hard d2fcb43* avanzar la rama main hasta ese commit y que se modifíque el working copy con lo que había en ese commit.
(*Creo que, desde main, podría haber hecho el reset -- hard a d2fcb43, y se quedarían unidas sin tener que haber creado la rama title otra vez*).

- ¿Qué comando o comandos usaste en el paso 32?

*git log* Para buscar el primer commit, 
*git checkout ...* para moverme al primer commit

- ¿Qué comando o comandos usaste en el punto 33?

*git reflog* Para buscar el ultimo commit donde se creo el titulo,
*git checkout ...* para moverme al ultimo commit.
