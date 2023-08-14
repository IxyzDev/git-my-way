# Guía Completa de Git

## Introducción a Git

Git es un sistema de control de versiones distribuido que permite rastrear los cambios en los archivos a lo largo del tiempo. Fue creado por Linus Torvalds en 2005 y se ha convertido en una herramienta fundamental para el desarrollo de software y la colaboración en proyectos.

## ¿Qué es un Sistema de Control de Versiones?

Un sistema de control de versiones (VCS) es una herramienta que ayuda a rastrear los cambios realizados en los archivos a medida que evolucionan. Permite a los equipos de desarrollo trabajar juntos de manera eficiente y mantener un historial completo de los cambios.

## Conceptos Básicos de Git

### Repositorio

Un repositorio de Git es un espacio donde se almacenan todos los archivos y su historial de versiones. Puede estar en local en tu computadora o en un servidor remoto.

### Commit

Un commit en Git es un punto en el tiempo que captura el estado actual de los archivos en el repositorio. Cada commit tiene un mensaje que describe los cambios realizados.

### Rama (Branch)

Las ramas en Git permiten crear líneas de desarrollo separadas. Puedes crear una rama para trabajar en una nueva característica sin afectar la rama principal (normalmente llamada "master" o "main").

### Fusión (Merge)

La fusión en Git combina los cambios de una rama en otra. Se utiliza para combinar el trabajo de diferentes ramas en una sola.

### Clonar (Clone)

Clonar un repositorio significa hacer una copia completa del repositorio en tu computadora. Esto te permite trabajar localmente y luego sincronizar los cambios con el repositorio remoto.

### Repositorio Remoto

Un repositorio remoto es una versión de tu repositorio alojada en un servidor en línea, como GitHub o GitLab. Permite la colaboración entre varios desarrolladores.

## Configuración Inicial

Antes de comenzar a usar Git, es importante configurar tu nombre y dirección de correo electrónico para que los commits se identifiquen correctamente. Puedes hacerlo usando los siguientes comandos:

```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tu@email.com"
```

Inicializar la rama principal siempre como main

```bash
git config --global init.defaultBranch main
```

## Comandos Básicos de Git

- `git init`: Inicializa un nuevo repositorio local.
- `git clone <url>`: Clona un repositorio remoto en tu computadora.
- `git add <archivo>`: Agrega un archivo al área de preparación.
- `git commit -m "Mensaje"`: Crea un nuevo commit con los archivos en el área de preparación.
- `git status`: Muestra el estado actual de los archivos en tu repositorio.
- `git log`: Muestra el historial de commits.
- `git branch`: Muestra las ramas disponibles y resalta la rama actual.
- `git checkout <rama>`: Cambia a una rama específica.
- `git merge <rama>`: Fusiona una rama en la rama actual.

## Colaboración y Repositorios Remotos

- `git remote add <nombre> <url>`: Agrega un repositorio remoto.
- `git push <nombre-remoto> <rama-local>`: Envía tus commits al repositorio remoto.
- `git pull <nombre-remoto> <rama-remota>`: Obtiene los cambios del repositorio remoto.
- `git fetch <nombre-remoto>`: Obtiene los cambios del repositorio remoto sin fusionarlos.

## Algunos alias

Una forma mas comoda de trabajar con git log

```bash
git config --global alias.lg "log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all"
```

Una forma mas comoda de trabajar con git status

```bash
git config --global alias.s status --short
```

## Conclusiones

Git es una herramienta esencial para el desarrollo de software y la colaboración en equipo. A través de su sistema de control de versiones, ramas y colaboración en repositorios remotos, Git facilita la gestión de cambios y la construcción conjunta de proyectos. ¡Empieza a explorar y a utilizar Git para potenciar tus proyectos de desarrollo!
