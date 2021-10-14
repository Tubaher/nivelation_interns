# Upload frames and report results

**NOTA:** Recordar que lo que se ha hecho hasta el momento es:
1. Grabar videos de 1 hora, de cámaras de seguridad de entradas y salidas de autos
2. Bajar dichos videos y editarlos para que solamente quede cuando entren y salgan vehículos
3. Volver a subir el nuevo video solamente de la entrada y salida de autos *(Usualmente de 1 hora se llegan a obtener entre 5 a 10 min de video de autos)*
4. Ahora separamos el video en algunos frames con
<!-- -->
    get_frames.py
5. Dependiendo la cantidad de imágenes se lo hace un zip o se usa ( en caso de más de 800 captures):
<!-- -->
    split_folder1.py

(Para contar los elementos se puede usar)
<!-- -->
    ls -1 | wc -l

6. Bajamos los archivos y los subimos al drive para que los etiqueten. A la dirección de:
<!-- -->
    LPRTeam/Quicentro Norte/unlabeled detection

7. Ahora a alguien los debe etiquetar y subir a la dirección: 
<!-- -->
    LPRTeam/Quicentro Norte/labeled detection/Carpeta/YOLO

En las carpetas YOLO (que se encuentran en formato zip) se encuentra la imagen con un txt que tiene las coordenadas de los labesls

8. Ahora vamos a VSC para ejecutar otro código para hacer 'crop' de nuestras 'plates', es decir recortar solo las placas a partir de los etiquetados
   
9.  Subimos nuestro zip con imágenes y los archivos YOLO a la siguiente dirección 
<!-- -->
    buscar dirección

10. Creamos la carpeta donde irán nuestros nuevos plates y cambiamos los paths antes de ejecutar el code
    
11. Ejecutamos el code:
<!-- -->
    crop_plates.py

12. Comprimimos en un zip nuestras placas recortadas y las guardamos en la siguiente dirección:
<!-- -->
    LPRTeam/Quicentro Norte/unlabeled plates

13. Ahora nuevamente alguien debe etiquetar las placas es decir colocar su número y volverlas a subir etiquetadas en la siguiente dirección:
<!-- -->
    LPRTeam/Quicentro Norte/labeled plates







