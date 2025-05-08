# Rama main

No usar rama master, cambiar siempre a main, esta rama debe ser la principal, la que se sube a producción, es por esto mismo que no deben de hacerse cambios directos en esta rama, siempre se debe de crear una rama nueva para hacer cambios y luego hacer un merge a la rama main.

# Solucionar problema de waring LF by CRLF
```
git config core.autocrlf true
```

# Merge - Uniones

> Fast forward merge: Es cuando el merge se une sin problemas con la rama principal, es decir, no hay conflictos y se puede hacer un merge sin problemas.
> Automatic merge: Es cuando el merge se une sin problemas con la rama principal, es decir, no hay conflictos y se puede hacer un merge sin problemas.
> Manuak merge: Es cuando el merge no se puede hacer automaticamente, es decir, hay conflictos y se debe de resolver manualmente.
> Merge conflict: Es cuando el merge no se puede hacer automaticamente, es decir, hay conflictos y se debe de resolver manualmente.