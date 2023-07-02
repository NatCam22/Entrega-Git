Respuesta a las preguntas:
- Comandos ejercicio 11: git reset --hard HEAD~1. Con este comando hacemos un 
reset que mueve head y main a HEAD~1 que deja inalcanzable el último commit (lo "deshace" y al hacer el --hard también borramos los cambios del working copy.
-Comandos 12: Buscamos el id del commit inalcanzable con un *git reflog*. Luego nos movemos a ese commit con *git reset <id del commit "deshecho">. 
- 13: No se realiza ningún merge al intentar hacerlo ya que no hay cambios que absorber. La rama master está en un commit anterior que es alcanzable por styled entonces al intentar hacer un merge sale que ya todos los commits son alcanzables y por tanto no hay nada que mergear. 
- Merge 19: Sí hay un conflicto ya que hay dos commits que modifican las mismas líneas de maneras diferentes. 
- Merge 21: No genera ningún conflicto, el merge es fast-forward (y por tanto no puede generar ningún conflicto, es como hacer una actualizació, o cambio, normal).
- Comandos 25: git log --graph --branches --oneline
- Merge 26: Sí podía hacerse un merge ff y que master apuntaba a un commit alcanzable por la rama title. 
- Comandos 27: git reset HEAD~1.
- Comandos 28: git restore git-nuestro.md.
- Comandos 29: git branch -D title.
- Comandos 30: git reflog (para ver el id del commit inalcanzable) + git reset <id del commit>
- Comandos 32: git reset <id del commit que buscábamos> (el id se encuentra gracias al mismo reflog de la instrucción anterior).
- Comandos 33: git restore git-nuestro.md porque el working copy tenía cambios no guardados y que no se querían guardar) + *git reset* al id del último commit + git restore de nuevo para no quedar con el working copy con cambios. 
