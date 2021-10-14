## Extract videos, edit, separate into frames
***
-   Una vez grabados nuestros videos vía **SSH** en la terminal de **Windows Poweshell** en **Windows Terminal**, nos conectados vía **SFTP** en otra pestaña con **Windows Poweshell** para extraer los videos
-   Cambiamos de directorio a donde se encuentra nuestro video grabado
<!-- -->
    cd /home/omia/Videos/plates

-   Verificamos que se encuentren nuestros videos
<!-- -->
    ls
    
-   Ahora nos ubicamos en nuestro directorio local
<!-- -->
    lls

-   Cambiamos nuestro directorio local al escritorio o *'Desktop'* para mayor facilidad
<!-- -->
    lcd Desktop/
- Ahora copiamos el video de nuestra carpeta anterior (Videos/plates/) donde lo habíamos guardado
***
**IMPORTANTE**: Fijarse que en directorio también a donde se encuentran los videos, es decir:
- Vía *ssh* ubicado en:
<!-- -->
    enomia@omia-B560M-DS3H:~/Videos/plates$
- Vía local ubicado en:  
<!-- -->
    C:\Users\Username\Desktop
Ambos en **Windows PowerShell** en **Windows Terminal**
***
- Ubicarnos en nuestro *'Desktop'* que se encuentra conectado vía *sftp* y colocar **get** y el archivo:
<!-- -->
    get nombre_del_archivo.mp4

Ahora esperamos que lo baje a nuestro escritorio
***
-   Una vez en nuestro escritorio editamos el video y solamente dejamos cortes donde aparezcan placas de auto
-   Donde se empiece a ver el número de placa y donde se empiece a dejar de ver

***
Ahora con nuestro nuevo video solamente de cortes de placas, vamos a subirlo a la máquina de Amazon procesar los códigos y obtener frames del video 
-   Abrimos **Visual Studio Code**
-   Clic en *'Open a Remote Window'* (flechas verdes, parte inferior izquierda)
-   Connect to Host... -> pract_ec
-   Abrimos una nueva terminal *(Notar que ya estamos conectados a la máquina de Amazon)*
-   Cambiamos de directorio a donde se encuentran nuestros videos previamente grabados
<!-- -->
    cd LPRProject\dataset.quicentro\videos_de_prueba_patentes
-   Cargamos el code de:
<!-- -->
    code get_frames.py
-   Activamos el enviroment **lpr** en el que vamos a ejecutar nuestros codes
<!-- -->
    conda activate lpr

Antes de ejecutar nuestro código creamos una carpeta que contenga los frames para añadirlo al path de *get_frames.py*
-   Abrimos un nuevo terminal
-   Ahora cambiamos el directorio a:
<!-- -->
    cd LPRProject/dataset.quicentro/videos_de_prueba_patentes/eval_det

-   Creamos una carpeta donde guardar nuestros frames
-   Por ejemplo creamos una carpeta X:
<!-- -->
    mkdir X
***
Antes de proceder y ejecutar nuestro código debemos subir nuestro video
-   Abrimos en **Windows Terminal** una pestaña de *Ubuntu*
-   Nos conectamos vía *sftp* a la máquina de Amazon
<!-- -->
    sftp ubuntu@34.234.189.94

-   Ahora cambiamos de directorio a la ruta donde están los códigos que se van a ejecutar, para dejar nuestro video en esa dirección
<!-- -->  
    cd LPRProject/dataset.quicentro/videos_de_prueba_patentes/

-   Cambiamos nuestro directorio local de Ubuntu a nuestro *'escritorio'* de windows donde está nuestro video recortado a subir
<!-- -->  
    lcd /mnt/c/Users/Username/Desktop/

-   Verificamos que se encuentre el video
<!-- -->  
    lls

-   Colocamos nuestro video de nombre X 
<!-- -->  
    put X.mp4

-   Observamos que se empieza a subir a la ruta que colocamos antes
<!-- -->  
    Uploading X.mp4 to /home/ubuntu/LPRProject/dataset.quicentro/videos_de_prueba_patentes/X.mp4

***
-   Ejecutamos nuestro code *'get_frames.py'* (modificar direcciones en caso de ser necesario, también es necesario guardar el archivo si se modifica)
<!-- -->
    python get_frames.py

-   Ahora todos los frames generados deben estar guardados en nuestra nueva carpeta
-   Si se encuentra en un rango de 750 a 800 comprimimos en zip 
<!-- -->  
    zip -r example.zip original_folder

-   Y lo movemos a nuestra carpeta donde se encuentran nuestros zip
***
**NOTA:** En caso de generarse más de 800 frames, correr el siguiente code:

<!-- -->
    python  split_folder1.py
 
-   Separará las imágenes en 250 para cada zip
-   Ahora descargamos todos los zips
-   Los subimos a Google Drive y reportamos en el excel
