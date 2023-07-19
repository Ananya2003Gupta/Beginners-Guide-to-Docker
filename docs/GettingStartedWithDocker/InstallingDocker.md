[//]: # (2.1 Installing Docker)

Docker is available for different operating systems, including Windows, macOS, and Linux. Here's a step-by-step guide on how to install Docker on each platform:

## Installing Docker on Windows:
- Visit the Docker website and download the [Docker Desktop installer for Windows](https://docs.docker.com/desktop/install/windows-install/).
- Run the installer and follow the on-screen instructions. It will guide you through the installation process.
- During the installation, you may come across a configuration page. On that page, you might see an option called "Use WSL 2 instead of Hyper-V."
- If you are given this option, you can choose whether you want to use WSL 2 or Hyper-V as the backend for Docker.
However, it's important to note that not all systems support both options. If your computer only supports one of them, you won't be able to choose the other one.
- Once the installation is complete, Docker Desktop should be running, and you'll see a small Docker icon in your system tray.

## Installing Docker on macOS:
- Go to the Docker website and download the [Docker Desktop installer for macOS](https://docs.docker.com/desktop/install/mac-install/).
- Open the downloaded DMG file and drag the Docker icon to the Applications folder.
- Launch Docker from the Applications folder. You might be asked to provide your system password to complete the installation.
- Docker Desktop should now be installed and running. You'll see Docker icon in your menu bar.

## Installing Docker on Linux:
Installing [Docker on Linux](https://docs.docker.com/desktop/install/linux-install/) varies depending on the specific distribution you're using. Here's a general outline:

- Refer to your Linux distribution's package manager (e.g., apt for Debian/Ubuntu, yum for CentOS/RHEL) and follow the instructions specific to your distribution.
- For example, on Ubuntu, you can use the following commands:
``` 
sudo apt-get update 
```
``` 
sudo apt-get install ./docker-desktop-<version>-<arch>.deb 
```
- After the installation, add your user to the `docker` group to run Docker commands without using `sudo`:
``` 
sudo usermod -aG docker your_username 
```
- Log out and log back in to apply the group changes.
- Verify the installation by running the command:
``` 
docker version 
```

By following these step-by-step instructions, you should be able to install Docker on your respective operating system. It's essential to ensure that the installation process completes successfully before proceeding with other Docker-related tasks.