[//]: # (Container Networking)

Networking is a crucial aspect of Docker containerization as it allows containers to communicate with each other and with the outside world. Understanding container networking is essential for building distributed and interconnected applications. 


## Default Networking:
By default, Docker containers are isolated from each other and the host machine.
Containers can communicate with each other on the same Docker network using their IP addresses.


## Container Ports:
- Containers can expose ports to allow communication with services running inside them.
- Use the ` -p` or `--publish` option with the docker run command to publish container ports to the host machine. For example:
```
docker run -p host-port:container-port image-name
```
- Replace host-port with the port number on the host machine and container-port with the port number inside the container.
- This allows external systems to access services running inside the container via the specified host port.


## Custom Networks:
- Docker provides the ability to create custom networks to connect containers.
- You can create a network using the `docker network create` command, specifying a name for the network. For example:
```
docker network create network-name
```
- Containers can be attached to the custom network during creation using the `--network` option with the docker run command. For example:
```
docker run --network network-name image-name
```
- Containers connected to the same custom network can communicate with each other using their container names as DNS names.


## Linking Containers:
- Linking allows one container to access the services exposed by another container.
- You can link containers using the `--link` option with the docker run command. For example:
```
docker run --link container-name:image-alias image-name
```
- Replace container-name with the name of the container you want to link and image-alias with an alias to reference the linked container.
- This establishes a secure channel between the containers, enabling them to communicate using the provided alias.


## DNS Resolution:
Docker provides built-in DNS resolution for container names within the same network.
Containers can resolve each other's names to their respective IP addresses without the need for manual configuration.