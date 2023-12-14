# docker_repo

Hi folks, please follow the below steps to complete the lab:

###### Step 1 - Build a docker image using the  below command: #####

sudo docker build . -t your_docker_user_id/pythonapp
##(note - change the above your_docker_user_id to userid you had created in cloud.docker.com)

sudo docker images
##the above command will list the images you built or pulled

sudo docker login
###enter your docker hub credentials

sudo docker push your_docker_user_id/pythonapp
##(note - change the above your_docker_user_id to userid you had created in cloud.docker.com)

###Stepp 2 - Run the application...

sudo docker run -p 8081:5000 --rm --name myfirstApp1 your_docker_user_id/pythonapp
###now go to browser enter the public dns name with port no 8081.

### if you would like to run on different port
sudo docker run -p 8091:5000 --rm --name myfirstApp2 your_docker_user_id/pythonapp
###Make sure port 8091 is allowed in security group rules of your EC2 instance.


##Below are some docker basic commands for your reference:(feel free to test them out later)

1. 'docker images' - this command will list all docker images you have on your machine.

2. 'docker search ubuntu' – search for the ubuntu image in docker registry

3. 'docker pull ubuntu' - pull the ubuntu image from docker registry

4. 'docker ps' - list all the running containers

5. 'docker ps -a' - list all the containers running and killed

6. 'docker run -it alpine /bin/sh' -  to run a container in interactive mode

7. 'docker stop <container_id>' - to stop a container from running

8. 'docker rm  <container_id>' - to remove/delete a stopped/killed container

9. 'docker rmi image_id' - to delete the images

10. 'docker run alpine ls -l' - to list content of a running container

11. 'docker run -it --rm -p 8088:8080 tomcat' - to run in interactive mode and expose container port

12. 'docker run -d nginx' - to run in detached mode

13. 'docker stop 6a3884fewwc6' - to stop/kill a container
