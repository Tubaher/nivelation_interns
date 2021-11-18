# Using deploy, roi and database of plates

1. Start docker
<!-- -->
    docker start omia

2. Exec docker
<!-- -->
    docker exec -it omia bash

3. Change direction to apps:
<!-- -->
    cd sources/app/sample_apps/

4. Enter to the lpr-app:
<!-- -->
    cd lpr-app/

5. Go to configs:
<!-- -->
    cd configs/ 

6. Now you can change the configs of 'lpr_config_deploy.txt'
<!-- -->
    nano lpr_config_deploy.txt

7. Change input **(source0)** and ouput **(sink1)** values

8. Also you have the nvds-analytics file (at the end of lpr_config_deploy.txt) you can enable or disable it

9. Return to configs/

10. Open 'analytics.txt'. In this file it is possible to find the ROI regions of each cam
<!-- -->
    nano analytics.txt

11. Leave configs/ directory
    
12. Open 'config_lpr.h'
<!-- -->
    nano config_lpr.h

13. In 'acceso_id' you can add the rest of the cameras 

14. For this last change you need to run (in lpr-app):
<!-- -->
    export CUDA_VER=11.1

15.  And also this run this line:
<!-- -->
    make

16. Then also in lpr-app directory run:
<!-- -->
    ./lpr-app -c configs/lpr_config_deploy.txt -t 

17. Now you can leave the docker
<!-- -->
    exit

***

18.  Now you can leave ecdev2 machine
<!-- -->
    exit

***
 
# Enter to the database of plates

1. Run in your terminal
<!-- -->
    psql --host=database-omia.ccco8vwbpupr.us-west-2.rds.amazonaws.com --port=5432 --username=digevo --dbname=postgres

2. Enter the password of the database
<!-- -->
    ********

3. Now you are in postgres

4. Run the next command:
<!-- -->
    select * from ingreso_vehiculo order by rd_id desc limit 100;

5. Copy the information and leave the db
<!-- -->
    /q

