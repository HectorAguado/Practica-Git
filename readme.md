### - ¿Qué comando utilizaste en el paso 11? ¿Por qué?

* `git reset —hard HEAD~1`

* `git reset HEAD~1` retrocede HEAD 1 commit en dirección al padre, pero con `--hard` decimos a git que deje el Working Copy vacío (como hacer reset y luego checkout)


### - ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?

* `git reflog`, para buscar el identificador hash del commit 

* `git reset --hard 889e22e`, con reset movemos puntero HEAD y su rama al commit. Con `--hard` dejamos el working copy vacío


### - El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
* No.
* Porque *master* ya formaba parte de *styled*


### - El merge del paso 19, ¿Causó algún conflicto? ¿Por qué? 
* Si.
* Porque existen diferencias en al menos una ocasión en las mismas líneas de _git-nuestro.md_ de ambas ramas


### - El merge del paso 21, ¿Causó algún conflicto? ¿Por qué? 
* No.
* Como *master* comparte el mismo grafo que *styled*, lo que ocurre (con un merge fast forward) es que se actualizan los cambios y la rama *master* se coloca a la altura de *styled*. Digamos que los cambios necesarios para la absorción, estan en el propio grafo.


### - ¿Qué comando o comandos utilizaste en el paso 25?
* `log --graph --decorate --pretty=oneline`


### - El merge del paso 26, ¿Podría ser fast forward? ¿Por qué? 
* Si.
* Como *master* comparte el mismo grafo que *title*, lo que ocurriría con un merge fast forward es que se actualizarían los cambios y la rama *master* se coloca a la altura de *title*. Digamos que los cambios necesarios para la absorción, estan en el propio grafo.


### - ¿Qué comando o comandos utilizaste en el paso 27?
* `git reset HEAD~1`


### - ¿Qué comando o comandos utilizaste en el paso 28? 
* `git checkout -- git-nuestro.md`


### - ¿Qué comando o comandos utilizaste en el paso 29? 
* `git branch -D title`


### - ¿Qué comando o comandos utilizaste en el paso 30? 
* `git reflog` para buscar el hash del commit del merge deshecho
* `git reset --hard 9762665`


### - ¿Qué comando o comandos usaste en el paso 32?
* `git log` para capturar el id del commit inicial
* `it checkout 27bcee8273e3587d3abbc39d9fe3f97afe0433f6` de esta forma no toco las ramas y muevo HEAD al commit inicial


###  - ¿Qué comando o comandos usaste en el punto 33?
* `git checkout master`, como *master* seguía en su sitio, solo tengo que volver a llevar a HEAD a su rama
 