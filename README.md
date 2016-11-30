# Practica_GIT
**Respuesta a las preguntas de la Practica para empezar a utlizar Git**

# ¿Qué comando utilizaste en el paso 11? ¿Por qué?

Utilizo `git reset --hard HEAD~1` para llevar la rama styled al padre, en este caso ~1 lleva al commit anterior al que me encuentro, utilizo --hard porque así pierdo los cambios realizados en el working copy.

# ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?

Utilizo `git reflog` para ver el SHA del commit anterior, una vez me aseguro cual es el SHA y pone el mensaje correcto ( para comprobar si me encuentro en el commit o no ) y hago un `git reset --hard 977fdf8` para rehacer los cambios en el working copy, una vez hecho esto, hago un `git log` para comprobar que estoy en el commit correcto.

# El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?

Primero compruebo con `git branch` que estoy en la rama styled, luego hago `git merge master`, el merge es fast forward porque los commit forman una lista, entonces styled contiene todos los commits de master por esta razón no causa ningun conflicto.

# El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?

Si, causa conflictos porque el archivo *git-nuestro.md* de la rama *htmlify* y el de la rama *styled* tienen distinto contenido e las mismas lineas del archivo por eso nos avisa que tenemos un conflicto. Solucionamos los conflictos, abriendo el archivo y solo nos quedamos con la parte de la rama *styled*.

# El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?

No causa ningun conflicto porque la rama *master* ya contiene todos los archivos de *styled*, por lo tanto solo tendria que avanzar la rama *master* a donde esta *styled* es un fast-forward porque es una lista.

# ¿Qué comando o comandos utilizaste en el paso 25?

`git log --graph --decorate --pretty=oneline`

# El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?

Si porque en el momento del commit desde la rama *title* es una lista, asique solo con desplazar la rama *master* a donde esta *title* contendria todos los commits de master.

# ¿Qué comando o comandos utilizaste en el paso 27?

Utilizo un `git reset HEAD~1`, para no perder los cambios del working copy.

# ¿Qué comando o comandos utilizaste en el paso 28?

Utilizo un `git checkout -- git-nuestro.md`, para descartar los cambios que aparecen en el `git-status`.

# ¿Qué comando o comandos utilizaste en el paso 29?

Utilizo el comando `git branch -D title` desde la rama *master* para borrar la rama *title*.

# ¿Qué comando o comandos utilizaste en el paso 30?

Utilizo `git reflog` y miro donde esta el merge y luego hago `git reset --hard e52edf5`.

# ¿Qué comando o comandos usaste en el paso 32?

Utilizo `git reflog` y miro donde esta y luego hago `git checkout 1efabd9`, aqui tambien se puede utilizar un `git reset`, ya que no especifica si queremos mover solamente el HEAD o la rama.

# ¿Qué comando o comandos usaste en el punto 33?

Utilizo `git reflog` y miro donde esta y luego hago `git checkout e52edf5`, aqui tambien se puede utilizar un `git reset`, ya que no especifica si queremos mover solamente el HEAD o la rama, luego me pinto el grafo para saber si esta todo bien con `git log --graph --decorate --pretty=oneline`
