Steps:
1. Create 2 new containers using the same image "rails". Now we have 3 containers: rcont1, rcont2, rcont3. Get the IP addresses of all 3 containers.

2. Again, make a copy of the default.conf file of nginx and make the following changes: 
    - Add an *upstream* element and include the IP addresses of the 3 containers as servers, as shown below:
  ![image](https://user-images.githubusercontent.com/106901908/229306219-3b861882-4893-4578-b121-65c0de825be8.png)  
    - In the *proxy-pass*, enter http://'name of the upstream element' . 
   
3. When I ran "localhost:8080", it told to add 'config.hosts >> "loadbalance" ' in the environment. I added it to the development.rb in the environments folder.

4. Then put in "localhost:8080" in the browser and the application worked.
