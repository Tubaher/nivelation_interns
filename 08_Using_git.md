## How to use Git and upload changes to Github
***
### Repositorio local (Git)
1. Crear una carpeta donde van a estar nuestro proyecto y sus archivos (codes, data, readme, etc.)
   
2. Todos nuestros archivos estarán en un área de **'no tracking'**

3. Ahora añadimos los archivos modificados a nuestra **'staging area'**
<!-- -->
    git add 'path_del_archivo'

**NOTA:** Agregar los cambios en grupo para luego comentarlos

4. Añadimos a nuestra **'branch'**, en este caso a la rama principal **'master'**
<!-- -->
    git commit -m 'comentario'

***
### Repositorio remoto (Github)
Ahora vamos a subir los cambios a nuestro **'repositorio remoto'**

5. En caso de haber cambios actualizamos nuestros archivos usando:
<!-- -->
    git pull origin 'nombre de la branch'

6. Ahora subimos nuestros cambios a nuestra rama principal:
<!-- -->
    git push origin 'nombre de la branch'

Ahora ya se suben los cambios a nuestra rama de desarrollo

**Nota:** En caso de usar una rama secundaria y no la master, y queremos que los cambios se apliquen a la rama master solicitamos un **'pull request'**
<!-- -->
    git pull request
