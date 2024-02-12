# Docker 
    it is virtualization software that makes development and deployment easier
    It packages applications with all necessary dependencies,system libraries and runtime

# Difference betweem docker and VM

Docker does not have it's own os and vm has it is own os 
Docker images are couple of MB and vm inages are couple of GB -size
Docker takes only few seconds to start where as VM takes few minutes to start -speed

Docker was mainly built for using in linux distribution but later they developed the docker desktop which uses the hypervisior platform and runs on windows.

Once docker is installed it has docker engine,docker cli and docker registry
Docker cli allows to interact with docker

Below are the commands used
 
 1. docker pull ngnix:1.23

     nginx - name of the image
     tag -1.23 (always mention the tag or else it will image the image with the tag latest)
 
 2. dokcer ps - it will list the images available

 3. docker run ngnix:1.23
      it will run the docker in the interactive mode to run the background mode use -d(detach)

 4. run the docker in the background mode
    
     docker run -d ngnix:1.23

 5. docker port binding: docker always runs in the isolated port mode to expose it to it the external network we need to port binding.

     docker run -d -p  8080:80 nginx:1.23

      where 8080 : it is port on the localhost where will expose the docker container
             80  : it is docker container port on which nginx runs

      it is always a standard practice to bind to the same port number on the localhost to the same number what it runs on the container

      for eg : in the container mysql runs on port 3306 and on the localhost also it should run on the same port -p 3306:3306

 6. docker ps - it will list all the containers that are running
    docker ps -a -it will list all the container that are availabe

7. docker start ,stop ,restart

    docker start containerid
    docker stop  containerid

8. Naming the docker container : when docker container gets started it provides some default name in order to avoid that we can give specific names required for us

  docker run --name web-app -d -p 8080:80 nginx:1.23

9. To collect the docker logs

   docker logs name of the container

10. command to build the docker image

    docker build -t node:1.0

     where t = tag



# public and private registries
  public
   docker hub is the biggest public repository on which images can be uploaded or downloaded
  
  private
    In differenet cloud providers there are different registries like on AWS we have ECR on which image can be strored in public and private repositories.


     
       
