[//]: # (Running the First Docker Container)

Now that you have Docker installed, let's run your very first Docker container. 
<br>
Running a container is the fundamental concept in Docker, allowing you to isolate and run applications in a portable and consistent manner. Here's a step-by-step guide to help you get started:

## 1. Pulling an Image:
Before running a container, you need an image.
An image is like a blueprint or template that contains all the necessary components and configurations for a specific application or service. 
Docker Hub is a popular registry that provides a vast collection of pre-built images. Here's how you can pull an image from Docker Hub:

- Open a terminal or command prompt.
- Use the `docker pull` command followed by the image name and tag to download the image. For example, to pull the official Nginx web server image, you can use:
```
docker pull nginx 
```
- Docker will retrieve the image from Docker Hub and store it locally on your machine. The download may take a few moments, depending on your internet speed.

## 2. Running a Container:
Now that you have the image, you can run a container based on it. Running a container allows you to start an instance of the application or service defined by the image. 

Here's how you can run your first Docker container:

- In the same terminal or command prompt, use the docker run command followed by the image name. For example, to run a container using the Nginx image you pulled earlier, you can use:
```
docker run nginx
```
- Docker will create a new container based on the image and start it. You'll see logs and information related to the container's execution.
- By default, the container runs in the foreground, and the terminal is attached to its output. You can stop the container by pressing `Ctrl+C`.

## 3. Accessing the Containerized Application:
Now that the container is running, you may want to access the application or service running inside it. Here's how you can do it:

- Open a web browser and enter `localhost` or `127.0.0.1` in the address bar.
- If the image you're using runs a web server, like Nginx, and exposes a port, you should see the default web page of the containerized application.
- To stop the container, go back to the terminal or command prompt where the container is running and press `Ctrl+C`.

<br>
Congratulations! You've successfully run your first Docker container. 

You can explore more images on Docker Hub, try running containers with different images, or even build your own images to containerize your applications.