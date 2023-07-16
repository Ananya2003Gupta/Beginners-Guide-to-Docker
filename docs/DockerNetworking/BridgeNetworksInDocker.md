[//]: # (Bridge Networks in Docker)
In Docker, a bridge network is a default networking mode that allows containers to communicate with each other on the same Docker host. It acts as a virtual switch that connects containers together and provides an isolated network environment.

## Default Bridge Network:
- When you install Docker, a default bridge network named bridge is created automatically.
- The default bridge network allows containers to communicate with each other using IP addresses.
- Each container connected to the default bridge network gets a unique IP address within that network.


## Container Communication:
- Containers within the same bridge network can communicate with each other directly.
- Docker assigns a unique IP address to each container within the network, allowing them to communicate using standard networking protocols.
- By default, containers can communicate with each other using their container names or IP addresses.


## Exposing Container Ports:
- Bridge networks allow you to expose specific ports from a container to the host machine or external networks.
- Exposing ports allows services running inside the container to be accessible from outside.
- When running a container, you can use the `-p` or `--publish` option to map container ports to specific host ports.


## Network Isolation:
- Bridge networks provide network isolation between containers.
- Containers on different bridge networks cannot communicate with each other directly, providing security and isolation for your applications.
- This isolation helps prevent unintended interactions between containers and ensures that each container operates independently.


## Connectivity to External Networks:
- Containers on a bridge network can also connect to external networks, such as the host network or other networks accessible to the host machine.
- This allows containers to interact with services running outside the Docker environment.
- By connecting containers to external networks, you can leverage existing network infrastructure and access external resources.


## User-Defined Bridge Networks:
- In addition to the default bridge network, Docker also allows you to create user-defined bridge networks.
- User-defined bridge networks provide more control and customization options for your container networks.
- You can create a user-defined bridge network using the docker network create command and specify the desired network characteristics.


## Integration with DNS Resolution:
- Docker provides built-in DNS resolution for containers on a bridge network.
- Containers within the same bridge network can use each other's container names as hostnames for communication.
- This simplifies communication between containers, as you can refer to other containers by their names instead of IP addresses.
Understanding bridge networks in Docker allows you to create isolated network environments for your containers and enable communication between them.