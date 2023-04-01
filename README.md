Step 1:
Pulled a mysql from docker and built a container "mysql-container".  
 sudo docker pull ubuntu/mysql  
 sudo docker run -d --name mysql-container -e MYSQL_ROOT_PASSWORD=mysql ubuntu/mysql:latest  
The ports are not published, to ensure that the database cant be accessed by the host.  
 
Step2:  
Configured the database.yml file:   
*Added the myql-container's IP address as host.   
*Added the password as given in the run command (MYSQL_ROOT_PASSWORD=mysql).  
*Now a connection is created between the database.yml file and the mysql container.  

Step3:  
Build the application image and run the container.  
A button appeared asking to create a database, and then to run 2 pending migrations. After that the website was working.
![image](https://user-images.githubusercontent.com/106901908/229294276-5fb0f201-d6ba-41a8-b139-b53c92fc6ba3.png)  
