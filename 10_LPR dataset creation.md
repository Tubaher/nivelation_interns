# LPR dataset creation

1. Upload **ALL** the zip and txt annotion files -> labeled_plates in the ecdev2 instance
<!-- -->
    /home/ubuntu/LPRProject/lpr_quicentro_norte/labeled_plates

**NOTE:** Both of them need to have the same name! The only difference is the extension (txt or zip)

2. Copy a .txt file from labeled_plates to one folder before
<!-- -->
    cp XXXX.txt ..

3. Run the code **lprannot**
<!-- -->
    python lprannot.py --path XXXX.txt 

4. This code gonna create the directory **'labels_plates'**
   
5. In **'labels_plates'** it's possible to see all the names of the .txt but, inside each txt the number of plate

6. Now copy the .zip file from labeled_plates to one folder before
<!-- -->
    cp XXXX.zip ..

7. Unzip the zip file
<!-- -->
    unzip XXXX.zip

8. Create two directories. The first one to save the images from the unzips and the second one to save all the txt files (just the first time)
<!-- -->    
    mkdir lpr_images_YYYYMMDD
    mkdir lpr_labels_YYYYMMDD

9. Now run from terminal the next code. This prevents the same names (images) from being repeated and just get the .jpg files
<!-- --> 
    rsync -ab --suffix ~.jpg -P folder_name/*.jpg lpr_images_YYYYMMDD/ 

10. In the **lpr_images_YYYYMMDD/** directory now it's all the images without repeated names (if that was the case)
    
11. Now run from terminal the next code. This prevents the same names (txt) from being repeated and just get the .txt files
<!-- --> 
    rsync -ab --suffix ~.txt -P labels_plates/*.txt lpr_labels_YYYYMMDD/

12. In the **lpr_labels_YYYYMMDD/** directory now it's all the txt files without repeated names (if that was the case)

13. Check if there is the same number of elements
<!-- --> 
    ls -l lpr_labels_YYYYMMDD/ | wc -l
    ls -l lpr_images_YYYYMMDD/ | wc -l

Probably no cause the images with no label txt where not deleted

14. Remove useless files
<!-- --> 
    rm XXXX.txt
    rm XXXX.zip
    rm -r labels_plates
    rm -r folder_name

Repeat the process with the next txt and zip file

