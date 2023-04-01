Step1:

1. Remove the existing application container and create a new container without publishing the ports (to ensure that the host cant access). Get the IP address of this container.

2. Pull nginx image from Docker Hub (sudo docker pull nginx)

3. Run the container , with port as 8080. (sudo docker run --name nginx-proxy -p 8080:80 nginx:latest)

4. Copy the default.conf file from the nginx-proxy container into another file.

5.  Insert a *proxy_pass* property with IP address of the application container as the value in the new file.
![image](https://user-images.githubusercontent.com/106901908/229303308-7d614f73-6211-4b02-864a-73c8f5f2bb1e.png)
 
6. Copy this file to "nginx-proxy:/etc/nginx/conf.d/" (overwriting the existing default.conf) and execute it and reload the container.

7. Run localhost:8080 to access the application through nginx reverse proxy.
