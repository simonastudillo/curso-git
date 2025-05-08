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