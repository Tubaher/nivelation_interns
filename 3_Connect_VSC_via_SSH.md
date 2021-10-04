## Documentation about how to use Visual Code with ssh
***
-   Abrimos **Visual Studio COde**
-   Vamos a extensiones
-   Instalamos Remote - SSH
-   Nos aparecerán unas flechas blancas con fondo verde, en la parte
    inferior izquierda de VSC (Open a remote window), le damos clic
-   Ahora aparece una lista, clic en ‘Open Configuration File’
-   Nos aparecerá un archivo config

<!-- -->

    # Read more about SSH config files: https://linux.die.net/man/5/ssh_config
    Host 
        HostName 
        User 

-   Abrimos **Windows Terminal**
-   Abrimos en una nueva pestaña un terminal de *Windows PowerShell*
-   Cambiamos de directorio a nuestra carpeta .ssh

<!-- -->

    cd .ssh

-   Copiamos nuestro archivo *omiag4v.pem* a nuestro actual directorio

<!-- -->

    cp C:/Users/otto0/Downloads/omiag4v.pem .

-   Verificamos que se encuentre en el directorio

<!-- -->

    ls

-   Generamos una key

<!-- -->

    ssh-keygen

-   Le damos a *‘enter’* 3 veces hasta regresar a nuestro directorio de
    .ssh
-   Revisamos que hay en nuestro directorio

<!-- -->

    ls

-   Abrimos el archivo *id\_rsa.pub*

<!-- -->

    cat id_rsa.pub

-   Copiamos y enviamos la key generada
-   Regresamos a **VSC**
-   Editamos nuestro archivo config (colocar la misma **ip**)

<!-- -->

    # Read more about SSH config files: https://linux.die.net/man/5/ssh_config
    Host pract_ec
        HostName XX.XXX.XXX.XX
        User ubuntu

-   Clic al botón de las flechas *Open a Remote Window*
-   Ahora en ‘Connect to Host’
-   Ahora clic en ‘pract\_ec’
-   Se abre una nueva ventada
-   Clic al botón de la derecha de las flechas de *Open a Remote Window*
-   Clic en terminal

### Ya nos conectamos via ssh mediante Visual Code
