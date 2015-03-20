# Uno

Al crear un repo git  con `git init` crea un directorio `.git` en la carpeta actual.

## ¿Qué hay de interesante ahí?

~~~
branches
config
description
HEAD
hooks
info
objects
refs
~~~

La mejor metáfora de como funciona git, es pensar en punteros, hay objetos guardados en donde están los
datos y punteros a esos objetos.

Los objetos, tienen a su vez, punteros a otros objetos (al commit anterior, por ejemplo).

HEAD, es el puntero al indice actual, el resto de los "*nombres*" de referencia, (como master, origin/master y v0.1)
están en refs:

~~~
heads
tags
~~~

los heads son las ramas.

## La magia del path

Cuando hacemos `git checkout feature31` busca una referencia a `feature31` en algun lado de refs (en algún
orden que considera aceptable), para especificar mejor a cual refirnos, tenemos que usar la ruta completa:
`git merge origin/master`.


