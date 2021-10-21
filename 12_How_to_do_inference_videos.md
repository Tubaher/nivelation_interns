# How to do inference videos

1. Enter to the **ds_2021_docker**
   
2. Go to
<!-- -->
    cd samples/configs/tlt_pretrained_models/lpr_config

3. Put your QA videos in the **sources_20211013** directory *(See 11_Using docker)*

4. Then we need to edit a txt file
<!-- -->
    deepstream_app_source1_detection_models.txt

5. Edit whith nano
<!-- -->
    nano deepstream_app_source1_detection_models.txt

6. Modify the input argument with the QA video that you want to infer

7. Modify the output argument with the name of the new infered video

8. <kbd>Ctrl</kbd> + <kbd>X</kbd> to leave the file. <kbd>Y</kbd> to save the changes and <kbd>enter</kbd> to leave
   
9.  Now run the modified file:  deepstream_app_source1_detection_models.txt
<!-- -->   
    deepstream-app -c file_name.txt

10. Then you can see the infered video on the output directory
    
11. Move the infered videos to **/ds** directory
    
12. Get the videos to see the accurate rate of each one