# Docker architecture

# Docker daemon -
Manage docker objects (images,containers,network,volumes) and listen to api requests. Communicate with other daemons.

# Docker client - 
This is the way docker user interacts with docker.It sends commands to api calls to docker daemon. It can communicate with more than one daemon.

# Docker registries - 
Stores docker images.(Example docker hub and docker client)

Docker objects - Example images, container,service.

# DockerFile -
FROM → Indicates base image
RUN -->Customize it by installing additional software
EXPOSE → Expose a port number for interaction
ENTRYPOINT → path

# Docker commands 

* How to push image to repository →
Save a state of image in different container 
Docker container commit id name

* Attach tag →
Docker tag imagename <tagname>  
tagname format is dockerhubid/repositoryname
  
* Push the image →
Docker login (login to docker hub)
Push <tagname>

* Docker save <imagename> > imagename.tar
Docker load < imagename.tar

* Docker image prune -->remove all tangling images
Docker image rm → delete specific image-->docker image rm <imagename>
Or
Docker rmi <imagename>

* Docker attach → It allow to interact with shell of container.(Attach StdIn to running container)
Note- you can come out using exit command, But it kills running instance.

* Docker exec-->Execute new command in running container.
Docker exec -i -t hidden-ubuntu bash
It create new process and do not attach existing one like attach,so exit command does not stop container instance.
* Docker inspect <dockerid> → inspect the container
Example ip address

* Docker container logs <containername>

* Debug→ View processes of running containers

* Docker container top <containername>

* Docker stop vs docker kill
Docker stop allows gracefully shutdown vs kill does forcefully.

* Docker container rename <existingname> <newname>
* Docker container diff command → shows what changes are done from container get created.
* Docker container commit → Save the changes and create new image.
* Docker container commit <containername> <newimagename>

* Mapping docker port to host machine port :

Docker run -d -i -t name httpd_1 -p 80:80 httpd

This maps port 80 of docker to port 80 of host

Docker run -d -i -t name httpd_2 -P  httpd
This command maps container exposed port to open port on host.

To see port settings
Docker container port <containername>
  
  

