# Alias para ver el log de git de forma más legible.
```
git config --global alias.lg "log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all"
```

# Alias para ver el status de git de forma más legible.
```
git config --global alias.s "status --short"
```

# Alias para ver el status de git de forma más legible y ver la información del branch activo.
```
git config --global alias.s "status --short --branch"
```