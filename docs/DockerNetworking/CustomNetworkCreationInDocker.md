[//]: # (Custom Network Creation in Docker)

In Docker, custom network creation allows you to create and manage your own networks for container communication and isolation. With custom networks, you have more control over the networking environment and can define how containers interact with each other.

## User-Defined Networks:
- Docker allows you to create user-defined networks using the docker network create command.
- User-defined networks are custom networks that you create to connect containers together.
- When creating a user-defined network, you can specify its name, subnet, IP address range, and other network-specific configurations.


## Network Types:
Docker supports different types of user-defined networks, including bridge networks, overlay networks, and MACVLAN networks.

1. Bridge networks: These networks are similar to the default bridge network in Docker and provide basic container communication and isolation.
2. Overlay networks: These networks enable communication between containers running on different Docker hosts, forming a distributed network across multiple hosts.
3. MACVLAN networks: These networks allow containers to have their own MAC addresses and appear as separate physical devices on the network.


## Network Drivers:
- Docker provides different network drivers that define how containers connect to and communicate within user-defined networks.
- Each network type has its own default driver, but you can specify a different driver during network creation.
- Bridge networks use the bridge driver by default, while overlay networks use the overlay driver.


## Container Connection to Custom Networks:
- Once you have created a custom network, you can connect containers to that network during their creation or afterward using the `--network` command.
- By connecting containers to a custom network, you allow them to communicate with other containers on the same network.
- Containers connected to the same network can use each other's container names or IP addresses for communication.

## Network Scopes and Isolation:
- Custom networks provide network scopes and isolation for your containers.
- Containers within a custom network can communicate with each other, but they are isolated from containers in other networks.
- This isolation ensures that containers on different networks cannot directly communicate with each other unless explicitly configured.


## Network Configuration and Management:
- Docker provides commands and options to manage and configure custom networks.
- You can inspect network details, modify network configurations, connect or disconnect containers from networks, and remove networks when they are no longer needed.