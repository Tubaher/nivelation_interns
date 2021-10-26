# Documentation about how to enter security cameras and retrieve videos

## Nos conectamos vía SSH a las cámaras para empezar a grabar

-   Descargar **AnyDesk** [(Clic aquí)](https://anydesk.com/es)
-   Abrimos **AnyDesk**
-   Colocamos en el recuadro vacío nuestro code: 
-   *QN: 349197840* o para *G: 756649794*
-   Colocamos nuestra clave: xxxxx
-   Clic al *'rayo'* en la parte superior de **AnyDesk**
-   Clic al menú de *'Configuración de Túnel TCP'*
-   Nos situamos en la parte superior en *'Tunnels for 349197840'*
-   En puerto local colocamos *'1000'* 
-   En puerto colocamos *'20'* 
-   Clic en *'guardar'*

***
-   Abrimos **Windows Terminal**
-   Nos conectamos vía **ssh** con nuestro puerto 1000
  <!-- -->
    ssh omia@localhost -p 1000

-   Escribimos *'yes'* (solamente aparece la primera vez que logeamos) y seguimos
  <!-- -->
    yes

-   Ingresamos nuestra contraseña
-   Ahora ya nos encontramos en:
<!-- -->
    omia@omia-B560M-DS3H

**NOTA:** Para ingresar o iniciar sesión, es necesario primero logearse en **AnyDesk** y luego logearse en el terminal de **Windows PowerShell** con:
  <!-- -->
    ssh omia@localhost -p 1000

***
-   Verificamos que estamos dentro del sistema:
<!-- -->
    ls

-   Ahora ingresamos a videos:
<!-- -->
    cd Videos/plates/

-   Deberíamos encontrar todos los videos hasta el momento grabados
<!-- -->
    omia@omia-B560M-DS3H

-   Le damos a <kbd>Ctrl</kbd> + <kbd>R</kbd> para ver los codes más usados
-   Vemos que aparece el siguiente code que es para grabar videos .mp4 de las cámaras y le damos a la tecla <kbd>&rarr;</kbd> para autocompletar
<!-- -->
    ffmpeg -i rtsp://192.168.30.2XX/channel1 xxxx.mp4

-   Reemplazar XX por el número de cámara que deseamos y xxxx por el nombre del archivo .mp4 a guardar
-   Vemos que aparece un cronómetro que indica el tiempo de grabación
-   Detener en 1 hora de grabación con <kbd>Ctrl</kbd> + <kbd>C</kbd>

***
## Ahora nos conectamos vía STFP a las cámaras para poder extraer los videos
-   Abrimos **Windows Terminal**
-   Abrimos una nueva pestaña de *'Windows Terminal'*
-   Nos logeamos vía nuestro puerto 1000
<!-- -->
    sftp -oPort=1000 omia@localhost

-   Ingresamos nuestra contraseña
-   Ahora ya nos encontramos conectados vía SFTP
