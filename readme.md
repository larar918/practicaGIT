# PRACTICA GIT 
**Alumno: Lara Rondón Ergueta**

**¿Qué comando utilizaste en el paso 11? ¿Por qué?**
Utilizamos el comando _git reset --hard HEAD~1_ ya que queremos eliminar el commit (modifica el graphic area) pero además queremos eliminar los cambios realizados en el fichero, por lo que debemos de modificar nuestro working copy.

**¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?**
Primero localizamos el identificador del commit realizado al cambiar el contenido del fichero mediante el comando _git reflog_.
Una vez identificado ejecutamos el comando _git reset --hard f3d4925(id del commit)_ para restaurar el commit y el fichero al estado deseado.

**El merge del paso 13, ¿Causó algún conﬂicto? ¿Por qué?**
Para realizar el mergeo utilizamos el comando _git merge main_  estando posicionados en la rama styled.
No se produce ningún conflicto ya que en main no se ha realizado ningún commit, no hay nada nuevo que no tenga ya el documento de la rama styled.

**El merge del paso 19, ¿Causó algún conﬂicto? ¿Por qué?**
Para poder realizar el merge debemos cambiarnos a la rama styled, que va a ser quien abosorba los cambios, mediante el comando _git checkout styled_.
Una vez en dicha rama ejecutamos el comando _git merge htmlify_.
En este caso el merge que se produce es de tipo no-fast-forward, lo que quiere decir que se creará un commit nuevo con los cambios. Como los ficheros son diferentes crea un conflicto que arreglamos editando el fichero y dejando solo el contenido que nos interesa, en este caso el styled.
Una vez modificado lo subimos al staged area y realizamos el un commit para que se termine de realizar el merge.

**El merge del paso 21, ¿Causó algún conﬂicto? ¿Por qué?**
En este caso, de nuevo, no se produce ningún conflicto. Esto se debe a que el merge es de tipo fast-forward.

**¿Qué comando o comandos utilizaste en el paso 25?**
Usamos el comando _git log --graph --oneline_

**El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?**
Si, ya que si se realiza ese tipo de merge el puntero de la rama main se movería al commit de la rama title y no perdería acceso a ninguno de los commits creados a lo largo del ejercicio.

**¿Qué comando o comandos utilizaste en el paso 27?**
Como el merge se ha hecho de forma no-fast-forward se ha creado un commit nuevo, por lo que para eliminarlo debemos del volver al commit anterior con el comando _git reset HEAD~1_.

**¿Qué comando o comandos utilizaste en el paso 28?**
Para eliminar los cambios en el fichero y modificar el working copy utilizamos el comando _git restore git-nuestro.md_.

**¿Qué comando o comandos utilizaste en el paso 29?**
Para eliminar la rama title ejecutamos el comando _git branch -D title_.
Hay que utilizar la opción -D ya que se dejan commits innacesibles.

**¿Qué comando o comandos utilizaste en el paso 30?**
Obtenemos el id del commit asociado al merge mediante el comando _git reflog_.
Después ejecutamos el comando _git reset 49205c6(id_commit)_ y asi se reestablece tanto el merge como el contenido del fichero. 

**¿Qué comando o comandos usaste en el paso 32?**
Primero buscamos el id del commit con el comando _git log --oneline_.
Luego ejecutamos el comando _git reset 8f0356f(id_commit)_ y volvemos al punto de inicio. 
Si queremos también modificar el contenido del fichero al estado de ese commit ejecutamos el comando _git restore git-nuestro.md_

**¿Qué comando o comandos usaste en el punto 33?**
Buscamos el id del commit con el comando _git reflog_
Ejecutamos el comando _git reset 2c68802(id_commit)_.
Si queremos también modificar el contenido del fichero al estado de ese commit ejecutamos el comando _git restore git-nuestro.md_