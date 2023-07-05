# My-Portfolio using docker 
This is my portfolio web page , which is deployed on my local machine using docker and nginx.

# Steps which i followed to complete this project 
Installation 
https://docs.docker.com/engine/install/ubuntu/
https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-20-04

# Check list of all running containers
   docker ps   


# check list of all containers ( runing and stopped both ) 
   docker ps -a 

   
# check list of all docker images
  docker images 


# pull ubuntu image 
  docker run ubuntu  

# pull nginx image
  docker pull nginx  

# Running Nginx with exposed port 80 

  Docker run -p 8080:80 nginx   

# Running Nginx with custom content

  Docker run -p 8080:80 -v /user/manoj/desktop/containers/nginx:/usr/share/nginx/html nginx

 Here ,
    -v →volume
    /user/manoj/desktop/containers/nginx   → path of source code 
    /usr/share/nginx/html   →specific nginx html path
    Nginx  → nginx image



# Using path variable in volume mapping   

  Docker run -p 8080:80 -v $pwd:/usr/share/nginx/html nginx
  
---> Here, $pwd → path of your content 

# Running containers in background 

    Docker run -p 8080:80 -d -v $pwd:/usr/share/nginx/html nginx

 ---> Run in background use -d for run containers in background



## Screen record

