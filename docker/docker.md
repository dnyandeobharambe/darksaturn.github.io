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
