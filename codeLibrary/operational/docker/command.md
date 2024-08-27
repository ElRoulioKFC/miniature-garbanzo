## Docker Command Cheatsheet

Here are some useful niche Docker commands that can help you streamline your Docker workflow:

1. `docker system prune`: This command removes all unused Docker resources such as containers, images, networks, and volumes, freeing up disk space on your machine.

2. `docker exec -it <container_name> <command>`: Use this command to execute a command inside a running container. It allows you to interact with the container's shell and run commands as if you were inside it.

3. `docker cp <container_name>:<path_to_file> <local_destination>`: This command allows you to copy files or directories from a container to your local machine. It is useful when you need to extract specific files from a container.

4. `docker logs <container_name>`: Use this command to view the logs of a running container. It displays the output of the container's stdout and stderr, which can be helpful for troubleshooting issues.

5. `docker commit <container_name> <image_name>:<tag>`: This command creates a new image from a running container. It is useful when you want to save the changes made inside a container as a new image.

6. `docker stats`: Use this command to monitor the resource usage of your running containers. It provides real-time information about CPU, memory, and network usage, helping you identify resource-intensive containers.

7. `docker volume rm $(docker volume ls -q)` : This command remove all volumes.

8. `docker rm $(docker ps -a -q)`: This command remove all images.

9. `docker stop $(docker ps -aq)`: This command stop every runing container.

Remember to refer to the Docker documentation for more details on each command.
