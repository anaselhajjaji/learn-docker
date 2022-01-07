# Concept

To achieve isolation, docker uses the two Linux specific features below:
- Namespacing: used to isolate resources per process (or group of processes), resources are: Processes, Hard drive, Network, Users, Hostnames, Inter Process Communication
- Control Groups (cgroups): limit amount of resources used per process: Memory, CPU Usage, HD I/O, Network Bandwith

But what about the other OS (MacOS, Windows) concerning Namespacing and Control Groups?
- When docker is started, a Linux virtual machine is created and started, so using this Virtual Machine we're able to have Control Groups and Namespacing.
- The containers will run inside this virtual machine.

What is done when the image is instanciated to become container?
- The image = filesystem snapshot is copied to an isolated piece of hardrive reserved to the container
- Other resources are reserved and isolated for the container: RAM, CPU, Network ...
- The process is started using the defined startup command and will have access to isolated resources (RAM, CPU ...)

# Installation

## Windows

Docker works good with WSL2, usefull links:
- https://docs.microsoft.com/en-us/windows/wsl/install-win10
- https://docs.docker.com/docker-for-windows/wsl/

If WSL2 is not supported, we can still use Docker Toolbox (important note: it's deprecated).
https://github.com/docker/toolbox/releases

## Linux

- Ubuntu: https://docs.docker.com/install/linux/docker-ce/ubuntu/
- CentOS: https://docs.docker.com/install/linux/docker-ce/centos/
- Debian: https://docs.docker.com/install/linux/docker-ce/debian/
- Docker compose installation: https://docs.docker.com/compose/install/#install-compose
- Run without sudo: https://docs.docker.com/install/linux/linux-postinstall/#manage-docker-as-a-non-root-user
- Start on Boot: https://docs.docker.com/install/linux/linux-postinstall/#configure-docker-to-start-on-boot

