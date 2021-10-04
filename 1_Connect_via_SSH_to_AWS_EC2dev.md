## Documentation about how to connect with SSH to an Amazon EC2 dev instance
***
-   Abrimos **Windows Terminal**
-   Abrimos en una nueva pestaña un terminal de *Ubuntu*
-   Regresamos a home

<!-- -->

    cd

-   **NOTA:** Recibir el archivo *omiag4v.pem*
-   Copiar *omiag4v.pem* al actual directorio

<!-- -->

    cp /mnt/c/Users/Username/Downloads/omiag4v.pem .

-   Revisar que se encuentra el archivo en el directorio

<!-- -->

    ls

-   Creamos una carpeta *.ssh*

<!-- -->

    mkdir .ssh

-   Revisamos la nueva carpeta que estará oculta

<!-- -->

    ls -a

-   Movemos *omiag4v.pem* a la carpeta *.ssh*

<!-- -->

    mv omiag4v.pem .ssh/

-   Revisar que se haya movido *omiag4v.pem* a *.ssh*

<!-- -->

    ls

-   Entramos al directorio

<!-- -->

    cd .ssh/

-   Revisamos *omiag4v.pem* en su nueva dirección

<!-- -->

    ls

-   Cambiamos a modo escritura *omiag4v.pem*

<!-- -->

    chmod 400 omiag4v.pem

-   Revisamos *omiag4v.pem* (Cambia de color ahora está blanco)

<!-- -->

    ls

-   Regresamos a nuestro directorio principal

<!-- -->

    cd

-   Nos conectamos a Amazon EC2 (La dirección **ip** debe ser enviada
    antes)

<!-- -->

    ssh -i .ssh/omiag4v.pem ubuntu@XX.XXX.XXX.XX
