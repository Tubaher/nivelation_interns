# Documentation about how to generate SSH keys: public, and private

-   Abrimos **Windows Terminal**
-   Abrimos en una nueva pestaña un terminal de *Ubuntu*
-   Regresamos a home

<!-- -->

    cd

-   Verificamos nuestras carpetas ocultas (debe estar .ssh)

<!-- -->

    ls -a

-   Cambiamos de directorio a nuestra carpeta ssh

<!-- -->

    cd .ssh

-   Generamos una key

<!-- -->

    ssh-keygen

-   Le damos a <kbd>Enter</kbd> 3 veces hasta regresar a nuestro directorio de
    .ssh
-   Revisamos que hay en nuestro directorio

<!-- -
    ls

-   Abrimos el archivo *id\_rsa.pub*

<!-- -->

    cat id_rsa.pub

-   Copiamos y enviamos la key generada
-   Regresamos a home

<!-- -->

    cd

-   Nos logeamos (colocar la misma **ip**)

<!-- -->

    ssh ubuntu@XX.XXX.XXX.XX

### Ya estamos conectados con Amazon EC2 vía ssh

## Ahora para ingresar vía sftp

-   Abrimos en una nueva pestaña un terminal de ubuntu
-   Regresamos a home

<!-- -->

    cd

-   Nos conectamos

<!-- -->

    sftp ubuntu@34.234.189.94

### Ya estamos conectados con Amazon EC2 vía ssh
