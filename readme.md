#GIT-NUESTRO

Hola Alberto. Ademas de este fichero incluyo tambien en el repositorio otro fichero llamado readme.rtf
Este otro fichero tiene el resultado de cada comando ejecutado en cada uno de los puntos. Lo pongo en un fichero aparte, porque al meterlo en este fichero de markdown, descuadraba todo el formato (por tener algunos asteriscos de las ramas y los saltos de linea van distintos y demas...) Por eso me ha parecido mejor ponerlo en un fichero aparte y en caso de que te surjan dudas en algun punto de la practica, puedas consultarlo.

Gracias y un saludo,

			Luis Mª Tolosana

##Ejercicio:					

- ¿Qué comando utilizaste en el paso 11? ¿Por qué?

$ git reset --hard HEAD~1

Con este comando deshago el ultimo commit y me voy al commit padre (HEAD~1). Ademas al poner “—hard” deshago los cambios realizados en el working copy.


- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?

$ git reflog

$ git reset --hard HEAD@{1}

Con el “git reflog” podemos saber por donde ha pasado el puntero HEAD para así poder volver al commit del punto 10 con el “git reset —hard HEAD@{1}”. En vez de usar la referencia de por donde había pasado HEAD en su movimiento anterior (HEAD@{1}), también podríamos haber usado el hash (a52862d) creado al hacer el commit del punto 10 que también nos da el “git reflog”.

PD: Alberto, en este punto no se si te referías a hacer esto o a volver a hacer un nuevo commit.


- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?

$ git merge master

No hay ningun conflicto porque no ha habido ningun cambio en master. Todo lo que hay en styled es una “evolución” de lo que había en master sin que haya habido ningun otro cambio en master. Es decir, realmente no se hace el merge, porque styled esta mas evolucionado que master.


- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?

$ git checkout styled

$ git branch

$ git merge htmlify

$ git status

$ vi git-nuestro.md

$ git add git-nuestro.md

$ git commit

Si, hay un conflicto porque el mismo fichero ha sido modificado en ambas ramas, tanto en styled como en htmlify.
Ademas, como las ramas no forman una lista, el merge es NO Fast Forward


- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?

$ git checkout master

$ git merge styled

No, no hay ningun conflicto porque el fichero no había sido modificado en la rama master. Ademas, como en este caso si que forman una lista, el merge si que es FF


- ¿Qué comando o comandos utilizaste en el paso 25?

$ git log --graph


 - El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?

$ git merge --no-ff title

Si, este merge podria haber sido FF porque ambas ramas formaban una lista


- ¿Qué comando o comandos utilizaste en el paso 27?

$ git reset HEAD~1


- ¿Qué comando o comandos utilizaste en el paso 28?

$ git status

$ git checkout -- git-nuestro.md 

$ git status 


- ¿Qué comando o comandos utilizaste en el paso 29?

$ git branch

$ git branch -D title

$ git branch


- ¿Qué comando o comandos utilizaste en el paso 30?

Con lo de “rehacer el merge” entiendo que te refieres a que volvamos al punto en el que hicimos ese merge.

$ git reflog

$ git reset --hard 8d30e47


- ¿Qué comando o comandos usaste en el paso 32?

$ git log

$ git reset --hard a35176b54abe80b0ead9d11dabbc57ae81b9f41e

$ git log



- ¿Qué comando o comandos usaste en el punto 33?

$ git reflog

$ git reset --hard 8d30e47

$ git log





