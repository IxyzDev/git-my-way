# Git Shortcuts

### ¿Qué es un Git Shortcut?

Un Git Shortcut es un comando personalizado que permite automatizar tareas comunes y repetitivas en Git. Son útiles para simplificar acciones como añadir un archivo .gitignore, realizar commits, o visualizar el historial de commits en un formato específico, agilizando tu flujo de trabajo.

---

### ¿Cómo se crean los Git Shortcuts?

Para crear un shortcut en Git, usamos el comando `git config --global alias.<nombre-del-alias> "<comando>"`, donde `<nombre-del-alias>` es el nombre que deseas para el alias y `<comando>` es el comando de Git que deseas acortar.

Por ejemplo:

```bash
git config --global alias.pyignore '!curl -o .gitignore https://raw.githubusercontent.com/github/gitignore/main/Python.gitignore'
```

Este comando crea un alias llamado `pyignore` que, al ejecutarse, descargará un archivo `.gitignore` para proyectos de Python en el directorio actual.

---

### ¿Dónde se guardan los Git Shortcuts?

Los shortcuts creados se guardan en el archivo de configuración de Git ubicado en tu carpeta de usuario, típicamente en `~/.gitconfig`. Este archivo contiene todos los alias configurados a nivel global y se puede editar manualmente si deseas hacer ajustes o eliminar alias específicos.

---

### ¿Cómo se eliminan los Git Shortcuts?

Para eliminar un alias de Git, utiliza el siguiente comando:

```bash
git config --global --unset alias.<nombre-del-alias>
```

Por ejemplo, para eliminar el alias `pyignore`, usarías:

```bash
git config --global --unset alias.pyignore
```

Este comando elimina el alias globalmente, haciendo que ya no esté disponible para tus repositorios.

---

### Índice de Shortcuts

A continuación, encontrarás una lista de shortcuts organizados en categorías según su funcionalidad.

[git-shortcuts](#git-shortcuts)

---

### Ejemplos de Git Shortcuts

#### Git Ignores

1. **Alias `pyignore` para proyectos de Python**

   Este shortcut permite generar un archivo `.gitignore` para proyectos de Python rápidamente.

   **Creación del alias**:

   ```bash
   git config --global alias.pyignore '!curl -o .gitignore https://raw.githubusercontent.com/github/gitignore/main/Python.gitignore'
   ```

   **Uso del alias**:

   ```bash
   git pyignore
   ```

   Al ejecutar este comando, se descargará un archivo `.gitignore` configurado específicamente para Python en el directorio actual.

