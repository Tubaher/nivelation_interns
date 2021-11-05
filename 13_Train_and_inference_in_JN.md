# Train and inference in Jupyter Notebook

1. Connect via SSH to EC AW2
   
2. Go to
<!-- -->
    cd tlt_cv_samples_vv1.1.0/

3. Type
<!-- -->
    screen -S jypter

4. Activate conda
<!-- -->
    conda activate

5. Enter to jupyter notebook
<!-- -->
    jupyter notebook --ip 0.0.0.0 --port 8888 --allow-root

6. Press <kbd>Ctrl</kbd> + <kbd>A</kbd> and <kbd>D</kbd>

8. See if Jupyter is running
<!-- -->
    screen -ls

9. Enter to explorer and type the direction and the port:
<!-- -->
    34.234.189.94:8888

10. Change directory:
<!-- -->
    lprnet/

11. Open **"lprnet.ipynb"**
    
12. Put your images to infer at:
<!-- -->
    lprnet/local/data/lpr_quicentro/val/image/

13. Put your labels at:
<!-- -->
    lprnet/local/data/lpr_quicentro/val/label/

**IMPORTANT:** Each image .jpg must have his respective .txt file with the same name, but inside de plate number of the corresponding image.

14. Run **5. Inferences** in **lprnet.ipynb**
    
15. The outputs are the results of the inference of each plate.