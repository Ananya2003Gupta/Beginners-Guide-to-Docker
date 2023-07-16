[//]: # (Container Lifecycle Management)

Managing the lifecycle of Docker containers is an important aspect of working with Docker. Understanding container lifecycle management allows us to control the creation, execution, and termination of containers effectively. Let's explore the container lifecycle and its management.

## Container Creation:
- Containers are created from Docker images, which serve as the blueprints for the containers.
- To create a container, you can use the `docker run` command followed by the image name. For example:
```
docker run image-name
```
- Docker searches for the specified image locally. If it doesn't find it, it automatically pulls the image from a registry like Docker Hub.
- You can also use the ‘docker create` command to create a new container from the specified image, without starting it. It is useful when you want to set up a container configuration ahead of time so that it is ready to start when you need it.

## Container Startup:
- When you run a container, it goes through the startup process, which involves initializing the container environment and executing the necessary commands.
- The container starts in the foreground by default, and you can see its output in the terminal.


## Interacting with Containers:
- Once a container is running, you can interact with it to perform various tasks.
- You can execute commands inside the container using the `docker exec` command. For example:
```
docker exec container-id command
```
- This allows you to run specific commands or access the container's shell to perform tasks within the container.
Stopping and Restarting Containers:
- To stop a running container, you can use the `docker stop` command followed by the container ID or name. For example:
```
docker stop container-id
```
- The container's execution is halted, and it moves to a stopped state.
- You can restart a stopped container using the `docker start` command followed by the container ID or name. For example:
```
docker start container-id
```

## Removing Containers:
- When you no longer need a container, you can remove it using the `docker rm` command followed by the container ID or name. For example:
```
docker rm container-id
```
- Removing a container permanently deletes it, and any data or changes made inside the container are lost.
- Use caution when removing containers, as data loss is irreversible.
Container Monitoring:
- Docker provides various commands and tools to monitor the status and performance of containers.
- The `docker ps` command lists the running containers, displaying information like container ID, image used, and status.
- You can use the `docker stats` command to monitor the resource usage of running containers, including CPU, memory, and network statistics.