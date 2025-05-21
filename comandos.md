# Primeros comandos de git

# 1. Obtener la versión de git instalada
```
git --version
```
# 2. Obtener ayuda de git
```
git help
```

# 3. Obtener ayuda de un comando específico
```
git help <comando>
```

# 4. Configurar el nombre de usuario y el correo electrónico
```
git config --global user.name "Tu Nombre"
git config --global user.email "tu email"
```

# 5. Ver la configuración actual de git
```
git config --list
```

# 6. Crear un nuevo repositorio
```
git init
```

# 7. Obtener el estado del repositorio
```
git status
```

# 7.1 Ver el estado abreviado del repositorio
```
git status -s
```

# 8. Agregar archivos al área de preparación (staging area)
```
git add <archivo> # Agregar un archivo específico
git add . # Agregar todos los archivos
```

# 9. Quitar archivos del área de preparación (staging area)
```
git reset <archivo> # Quitar un archivo específico
git reset . # Quitar todos los archivos
```

# 10. Hacer una fotografía del estado del repositorio (commit)
```
git commit -m "Mensaje del commit"
```
# 11. Volver el proyecto al último commit
```
git checkout -- .
```

# 11.1 Volver un archivo específico al último commit
```
git checkout -- <archivo>
```

# 12. Ver información de la rama
```
git branch
```

# 13. Cambiar el nombre de la rama default (master a main)
```
git config --global init.defaultBranch main
```

# 14. Guardar los cambios y agregar un mensaje al commit
```
git commit -am "Mensaje del commit"
```

# 15. Ver logs del repositorio
```
git log
```

# 15.1 Ver logs del repositorio en una sola línea
```
git log --oneline
```

# 16. Agregar todos los htmls al área de preparación (staging area)
```
git add *.html
```

# 17. Crear un nuevo alias para un comando
```
git config --global alias.<new comand> "<comando original>"
```

# 18 Ver las diferencias entre el último commit y el estado actual
```
git diff
```

# 19 Ver las diferencias entre el último commit y el estado actual incluyendo en el stage
```
git diff --cached
```

# 20 Modificar el mensaje del último commit
```
git commit --amend -m "Nuevo mensaje del commit"
```

# 21 Deshacer el último commit pero mantener los cambios en el área de preparación (staging area)
```
git reset --soft HEAD^
```

# 22. Volver en el tiempo a un commit específico
> Esto eliminará todos los cambios posteriores al commit especificado, así que ten cuidado al usarlo.
```
git reset --hard <commit>
```

# 23. Volver en el tiempo a un commit específico pero manteniendo los cambios en el área de preparación (staging area)
```
git reset --soft <commit>
```

# 24. Ver log de todo lo ocurrido en el repositorio
```
git reflog
```
# 25. Volver en el tiempo a un commit eliminado
> Puedes ver en reflog el commit eliminado y volver a ese commit.
```
git reset --hard <commit> 
```

# 26. Cambiar el nombre de un archivo
```
git mv <archivo viejo> <archivo nuevo>
```

# 27. Eliminar un archivo del repositorio y del sistema de archivos
```
git rm <archivo>
```

# 28. Crear una nueva rama
```
git branch <nombre de la rama>
```

# 28.1 Crear una nueva rama y cambiar a ella
```
git checkout -b <nombre de la rama>
```

# 29. Cambiar de rama
```
git checkout <nombre de la rama>
```

# 30. Unir una rama al main
> Es importante estar en la rama main para hacer el merge.
```
git merge <nombre de la rama>
```

# 31. Eliminar una rama
```
git branch -d <nombre de la rama>
```

# 32. Crear un tag
```
git tag <nombre del tag> <commit>
```

# 32.1 Crear un tag con un mensaje
```
git tag -a <nombre del tag> -m "Mensaje del tag" <commit>
```

# 33. Ver los tags
```
git tag # Ver los tags
```

# 34. Eliminar un tag
```
git tag -d <nombre del tag>
```

# 35. Ver el detalle de un tag
```
git show <nombre del tag>
```

# 36. Almacenamiento "temportal" de cambios (stash)
```
git stash # Almacenar los cambios
```

# 36.1 Almacenar cambios con un mensaje
```
git stash save "Mensaje del stash" # Almacenar los cambios con un mensaje
```

# 37. Ver los cambios almacenados
```
git stash list
```

# 37.1 Ver los cambios almacenados con detalle
```
git stash list --stat
```

# 38. Aplicar los cambios almacenados
```
git stash pop # Aplicar los cambios y eliminar el stash
```

# 39. Eliminar el stash
```
git stash drop # Eliminar el stash
```

# 40.1 Eliminar un stash específico
```
git stash drop <n> # Eliminar un stash específico
```

# 40. Eliminar todos los stashes
```
git stash clear # Eliminar todos los stashes
```

# 41. Recuperar un stash específico
```
git stash apply <n> # Recuperar un stash específico
```

# 42. Actualizar la rama con los nuevos cambios del main
```
git rebase main
```

# 43. Rebase interactivo
```
git rebase -i <commit> # Rebase interactivo
```

# 43.1. Rebase interactiva para fusionar commits
```
git rebase -i HEAD~<n> # Rebase interactivo para fusionar los últimos n commits
```
> Cambiar pick por squash o s para fusionar ese commit con el anterior.

# 43.2. Rebase interactivo para editar el comentario de un commit
```
git rebase -i HEAD~<n> # Rebase interactivo para editar el comentario de un commit
```
> Cambiar pick por reword o r para editar el comentario de ese commit.

# 43.3. Rebase interactivo para editar un commit
```
git rebase -i HEAD~<n> # Rebase interactivo para editar un commit
```
> Cambiar pick por edit o e para editar ese commit.

# 44. Agregar un repositorio remoto
```
git remote add <nombre> <url> # Agregar un repositorio remoto. ejemplo: git remote add origin
```

# 45. Ver repositorio remoto
```
git remote -v # Ver repositorio remoto
```

# 46. Subir cambios al repositorio remoto
```
git push <nombre remoto> <rama> # Subir cambios al repositorio remoto. ejemplo: git push origin main
```
# 47. Subir tags al repositorio remoto
```
git push --tags
```

# 48. Bajar cambios del repositorio remoto de la rama actual
```
git pull
```
# 49.1. Bajar cambios de una rama específica del repositorio remoto
```
git pull <nombre remoto> <rama> # Bajar cambios de una rama específica del repositorio remoto
```

#  49.2 Bajar cambios con conflictos
```
git pull --rebase # Bajar cambios con conflictos
```

# 49.3 Terminar el rebase
```
git rebase --continue # Terminar el rebase
```

# 49. Clonar un repositorio remoto
```
git clone <url> # Clonar un repositorio remoto
```