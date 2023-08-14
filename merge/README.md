# Guía de Fusiones (Merges) en Git

## Introducción a las Fusiones en Git

Las fusiones (merges) son una parte fundamental del flujo de trabajo en Git. Permiten combinar cambios de una rama a otra, lo que es esencial para trabajar en colaboración y mantener un historial de desarrollo coherente. En esta guía, aprenderás sobre los diferentes tipos de fusiones, cómo realizarlas y cómo manejar situaciones comunes que pueden surgir durante el proceso de fusión.

## Tipos de Fusiones

### Fusiones Directas (Fast-Forward)

Una fusión directa ocurre cuando no hay cambios adicionales en la rama de destino desde que se creó la rama que se fusionará. En este caso, Git simplemente avanza la rama de destino para incluir los commits de la rama fusionada. Esto es común cuando estás trabajando en una rama y actualizas tu rama principal.

### Fusiones de Tres Vías (Three-Way Merges)

Las fusiones de tres vías son más complejas y ocurren cuando hay cambios en ambas ramas, la rama de destino y la rama que se fusionará. Git utiliza un commit común, conocido como "commit base", para determinar qué cambios deben incluirse. Durante la fusión, Git crea un nuevo commit que combina los cambios de ambas ramas.

## Realizar una Fusión

1. **Actualizar tu Rama Principal**: Antes de fusionar, asegúrate de que tu rama principal (por ejemplo, `main` o `master`) esté actualizada con los últimos cambios. Puedes usar `git pull` para obtener los cambios más recientes.

2. **Cambiar a la Rama de Destino**: Utiliza `git checkout` para cambiar a la rama en la que deseas fusionar los cambios. Por ejemplo, `git checkout main`.

3. **Realizar la Fusión**: Ejecuta el comando `git merge <rama-a-fusionar>` para fusionar la rama deseada en la rama de destino.

    ```bash
    git merge feature-nueva
    ```

4. **Resolver Conflictos**: Si hay conflictos entre los cambios, Git te notificará. Abre los archivos con conflictos, resuelve las diferencias y luego haz `git add` para marcar los conflictos como resueltos.

5. **Completar la Fusión**: Después de resolver los conflictos, utiliza `git commit` para crear un nuevo commit de fusión. Git generará automáticamente un mensaje que puedes personalizar.

## Estrategias de Fusión Avanzadas

### Fusión Rebase

El rebase es otra forma de combinar cambios, pero en lugar de crear un commit de fusión, replantea la rama en la que estás trabajando sobre la rama de destino. Esto resulta en una historia de commits más lineal.

```bash
git checkout feature-nueva
git rebase main
```

### Fusiones con Fast-Forward Solo

Si deseas evitar la creación de commits de fusión, puedes usar la opción `--ff-only` para realizar solo fusiones directas.

```bash
git merge --ff-only feature-nueva
```

## Conclusiones

Las fusiones en Git son fundamentales para trabajar en equipo y mantener un historial de cambios coherente. A medida que adquieras experiencia con las fusiones, podrás manejar situaciones más complejas, como conflictos, y explorar estrategias avanzadas como el rebase. ¡Dominar las fusiones te permitirá colaborar de manera efectiva en proyectos y mantener un flujo de desarrollo fluido!