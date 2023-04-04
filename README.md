Steps:
1. Created a volume : sudo docker volume create dbvol


2. Removed the existing mysql-cont. Created a new container with added property : -v dbvol:/var/lib/mysql. 


3. Created a empty folder in the local host (named bind). 


4. Removed the existing nginx-proxy container and created a new container with added property : -v ~/Desktop/bind:/etc/nginx/conf.d 


5. Changed the default.conf file in the container. The change reflected in the "bind" folder in local host. 


6. The website worked on accessing localhost:8080.
