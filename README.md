Step1:
1. Pull nginx image from Docker Hub (sudo docker pull nginx)

2. Run the container , with port as 8080. (sudo docker run --name nginx-proxy -p 8080:80 nginx:latest)

3. Copy the default.conf file from the nginx-proxy container.

4.  Insert a *proxy_pass* property with IP address of the application container as the value.
![image](https://user-images.githubusercontent.com/106901908/229303308-7d614f73-6211-4b02-864a-73c8f5f2bb1e.png)
 
5. Remove the existing application container and create a new container without publishing the ports (to ensure that the host cant access).

6. Run localhost:8080 to access the application through nginx reverse proxy.
