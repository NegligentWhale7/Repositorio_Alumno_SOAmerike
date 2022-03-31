# Git
Es un software de versionado, útil especialmente para proyectos colaborativos.

---
## Flujo de trabajo de GitHub
Antes de crear un repositorio, se deben hacer un par de configuraciones globales, tales como el nombre del usuario, e-mail y un editor de texto, que no sea nano y atom, de forma que bloqueé la terminal hasta que no se cierre (para evitar cualquier inconveniente).

El e-mail deber ser de preferencia, el mismo que el de su cuenta de GitHub.

```
$ git config --global user.name ("nombre del usuario")
$ git config --global user.email ("e-mail de usuario")
$ git config --global core.editor "core --wait"
```
Para el flujo de trabajo desde la creación de la terminal se aplican los siguientes comandos:
```
$ git init
$ git add .
$ git commit -m ("Descripción para el commit")
$ git branch -M main
$ git remote add origin <URL al repositorio remoto en la página de GitHub>.git
$ git push -u origin main
```

Para vincular un repositorio ya existente:
```
$ git init
$ git branch -M main
$ git remote add origin <URL al repositorio remoto en la página de GitHub>.git
$ git pull origin main
$ git push -u origin main
```

El flujo de trabajo puede dividirse en 4 etapas:
1. Working Directory: Aquí se maneja el repositorio local; cambios sin guardar.
1. Staging area: Los cambios han sido añadidos.
1. HEAD: Se ha hecho un commit y está listo para ser subido.
1. Remote: Se encuantran el el repositorio remoto de GitHub.

![Flujo](https://bluuweb.github.io/tutorial-github/img/git-flujo.png)

### Ramas y versiones
Al usar repositorios puedes dividir el trabajo al trabajar en ramas externas a la principal, así divides el trabajo y evitas interferir con la rama principal.

```
$ git branch ("Nombre de la rama")
$ git checkout branch <"Nombre de la rama a la que cambiar">
```

Para fusionar ramas nos movemos a la principal y ejecutamos:
```
$ git merge ("Nombre de la rama")
```

Para crear una rama y cambiar a la misma en el mismo comando:
```
$ git checkout -b ("Nombre de la rama")
```

Existen un par de comandos para revisar los commits anteriores, al usarlos, la terminal te da un id que deberás usar si quieres volver a esa versión del repositorio:
```
$ git log
$ git log --oneline
$ git checkout ("id del commit")
```
El siguiente comando es importante para guardar los commits y sus id´s, y así poder regresar a la versión más reciente.

```
$ git log > ("nombre del documento").txt
```

### Regresar
:arrow_left: [README](README.md)