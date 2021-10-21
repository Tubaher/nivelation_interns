# Using docker

**Important commands:**
1. Connect vía **SSH** to EC2 (try to use VSC)
- Show active dockers
<!-- -->
    docker ps

- Show active + inactive dockers
<!-- -->
    docker ps -a

- Start docker (In this case the docker that we are gonna use **ds_2021**)
<!-- -->
    docker start ds_2021

- Exit the docker
<!-- -->
    docker exit

***
2. Execute the docker:
<!-- -->
    docker exec -it ds_2021 bash
(docker execute interactive docker_name aplication_name)

3. Change the directory to 
<!-- -->
    cd samples/configs/tlt_pretrained_models/lpr_config

4. Then make a directory to save our QA videos
<!-- -->
    sources_20211013

5. In a new window enter again to the **ds_2021** docker
   
6. Go to root and enter in ds directory
<!-- -->
    cd /ds

**IMPORTANT:** *ds* is a directory that is shared by Amazon EC2 and the docker. Then all the files that we want to share need to stay in this directory.

7. Upload the QA videos to the **ds** directory in Amazon EC2
   
8. Enter to the **ds** directory in root of the docker and move or copy to the directory that we want in this case 'sources_20211013'
<!-- -->
    cp XXXX.mp4 /samples/configs/tlt_pretrained_models/lpr_config/sources_20211013