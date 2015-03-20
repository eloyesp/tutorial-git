# Comandos

La cuestión de los comandos es que esto es software libre en serio, por lo que,
en general, los comandos hacen solo una cosa y delegan el resto. Por eso vamos
a encontrar comandos que son de bajo nivel y otros de alto nivel que reusan los
anteriores.

  - pull: es un ejemplo de comando de alto nivel, lo único que hace es fetch +
  merge / rebase (si se llama con --rebase)

  - fetch: actualiza las referencias locales de un remote, o sea, las
  referencias existentes en `refs/remotes/origin/master`

 - push: tiene un montón de configuraciones que afectan los defaults, pero la versión completa del comando es:
   `git push origin local_branch:remote_branch`, si uno omite algún dato, el resultado depende de la configuración.

   Si no indicamos un remote, el remote depende de la rama en la que estamos y su config:

        [branch "master"]
                remote = heroku

   Y en el peor de los casos usa el remote con nombre `origin`. Y cuales ramas pushea depende de otras config.

   De acá salen cosas interesantes, por ejemplo, que `git push origin :algo` **borra** la rama remota `algo`.

- checkout
- merge
- cherry-pick
- log
- rebase
- commit
- add
- rm
- diff
- show
- reflog
- rev-list
- revert
- stash
- remote
- branch
- tag

## config raras.

Me meto en un proyecto que tiene mil ramas y no quiero toda esa mugre...

~~~
[remote "horrible"]
	url = git@github.com:eloyesp/iot-sensor-simulator.git
	fetch = +refs/heads/development:refs/remotes/horrible/master
~~~
