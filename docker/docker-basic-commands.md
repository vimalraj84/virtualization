Command	Description	Example
docker pull 	docker pull command to download the image	
docker run	the Docker client finds the image , loads up the container and then runs a command in that container.	docker run hello-world
docker start	Starts one or more stopped containers	
docker stop	Stops one or more running containers	
docker exec	Runs a command in a run-time container	
docker exec -it <container name> <command>	to execute whatever command you specify in the container.	
docker exec -it <container name> /bin/bash	to get a bash shell in the container	
winpty 	If the input device is not a TTY. If you are using mintty, try prefixing the command with 'winpty'	winpty docker run -it ubuntu bash
		
		winpty docker exec -it postgres_db bash
docker build 
	Builds an image form a Docker file	
docker push 
	Pushes an image or a repository to a registry	
docker export	Exports a container’s filesystem as a tar archive	
docker search 
	Searches the Docker Hub for images	
docker attach 
	Attaches to a running container	
docker commdoit	Creates a new image from a container’s changes	
Ctrl+P+Q 	command to exit out of the container. It ensures that the container still exists even after we exit from the container.	
docker run --rm	the --rm flag automatically removes the container when it exits.	
docker ps	shows you all containers that are currently running	docker ps
docker ps -a	list of all containers that we ran. STATUS column shows that these containers exited a few minutes ago.	Docker ps -a
docker rmi <imageID>	This command is used to remove Docker images.	sudo docker rmi 7a86f8ffcb25 
docker rm	To clean up containers once I'm done with them	
		
docker images 		docker images –q
		
		q: It tells the Docker command to return the Image ID’s only.
docker rm $(docker ps -a -q -f status=exited)	This command deletes all containers that have a status of exited	
	
	-q flag, only returns the numeric IDs 
	
	-f filters output based on conditions provided
docker container prune	This will remove all stopped containers	
docker inspect Repository	used see the details of an image or container	Repository − This is the name of the Image.
docker history ImageID 	you can see all the commands that were run with an image via a container.	
docker system prune	Purging All Unused or Dangling Images, Containers, Volumes, and Networks	docker system prune -a
	
docker top ContainerID 	you can see the top processes within a container	docker top 9f215ed0b0d3
docker pause ContainerID 	used to pause an existing Docker container.	
docker unpause ContainerID	used to unpause an existing Docker container.	
docker kill ContainerID	used to kill an existing Docker container	
docker-compose run <container name> <command>	The proper way to run a command in a container	docker-compose run web /bin/bash

