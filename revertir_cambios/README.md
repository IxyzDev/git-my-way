# Revertir cambios en Git

## 1. Revertir cambios con `git revert`

Por supuesto, aquí tienes cómo revertir cambios usando `git revert`:

**Revertir cambios con `git revert`:**

`git revert` deshace los cambios de un commit específico creando un nuevo commit que revierte esas modificaciones. Esto mantiene el historial intacto y es seguro para entornos compartidos.

**Pasos:**

1. Identifica el hash del commit cuyos cambios deseas revertir.

2. Ejecuta el comando `git revert` seguido del hash del commit:

   ```bash
   git revert <commit-hash>
   ```

3. Git abrirá el editor para que puedas escribir un mensaje de confirmación para el nuevo commit que deshace los cambios. Simplemente guarda y cierra el editor.

4. El commit de revert será creado y los cambios serán deshechos.

**Ejemplo:**

Supongamos que deseas revertir los cambios del "Commit C":

```bash
git revert CommitCHash
```

Git creará un nuevo commit que deshace los cambios introducidos por "Commit C".

**Importante:** Al usar `git revert`, no estás eliminando el commit original ni cambiando el historial. En su lugar, estás creando un nuevo commit que deshace las modificaciones. Esto es útil para mantener un historial coherente y rastreable de los cambios realizados.

## 2. Volver a un commit anterior con `git reset`

`git reset` permite volver a un commit anterior y potencialmente eliminar commits. Es más poderoso y potencialmente riesgoso, especialmente si trabajas en un entorno colaborativo.

**Pasos:**

1. Identifica el hash del commit al que deseas volver.

2. Ejecuta el comando `git reset` con la opción adecuada según tu objetivo. Por ejemplo:

   - Si deseas eliminar los commits posteriores y volver al commit anterior:

     ```bash
     git reset --hard <commit-hash>
     ```

   - Si deseas conservar los cambios pero descartar los commits posteriores:

     ```bash
     git reset --soft <commit-hash>
     ```

**Ejemplo:**

Si deseas volver al estado de "Commit B" y descartar los commits posteriores:

```bash
git reset --hard CommitBHash
```

Esto moverá la rama actual al estado de "Commit B" y eliminará los commits posteriores.

Recuerda que `git revert` es más seguro y recomendado para entornos compartidos, mientras que `git reset` debe usarse con precaución, especialmente si ya has compartido tus commits con otros.
