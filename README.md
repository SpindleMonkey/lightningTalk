# Docker

[Docker](https://www.docker.com/) is a container platform that automates setting up development environments.

From the Docker website: "A container image is a lightweight, stand-alone, executable package of a piece of software that includes everything needed to run it: code, runtime, system tools, system libraries, settings. Available for both Linux and Windows based apps, containerized software will always run the same, regardless of the environment. Containers isolate software from its surroundings, for example differences between development and staging environments and help reduce conflicts between teams running different software on the same infrastructure."

Basically, containers are a way to isolate development from the environment.

## Background
- Launched in 2013
- 2015: Docker donated the specification and runtime code now known as runC, to the Open Container Initiative (OCI) to help establish standardization as the container ecosystem grows and matures.
- continues to give back with the containerd project. Containerd is the core container runtime of the Docker engine daemon, an industry-standard container runtime with an emphasis on simplicity, robustness and portability, designed as an embeddable component for higher level systems

Docker engine is built on containerd and runC

[containerd](https://containerd.io/): an industry-standard container runtime with an emphasis on simplicity, robustness and portability. It is available as a daemon for both Linux and Windows, which can manage the complete container lifecycle of its host system: image transfer and storage, container execution and supervision, low-level storage and network attachments

[Docker Open Source](https://www.docker.com/technologies/overview#/software_infrastructure)

Open Container Initiative: The Open Container Initiative is an open governance structure, formed under the Linux foundation, to create open industry standards for container formats and runtime.

runC: RunC is a CLI tool for spawning and running containers according to the OCI specification

** Terminology

* Images - The file system and configuration of our application which are used to create containers. You can think of an image like a Git repo; images can be committed with changes and you can specify a version if needed (if no version is specified, the default, or latest, version is used)

* Containers - Running instances of Docker images — containers run the actual applications. A container includes an application and all of its dependencies. It shares the kernel with other containers, and runs as an isolated process in user space on the host OS. 

* Docker daemon - The background service running on the host that manages building, running and distributing Docker containers.

* Docker client - The command line tool that allows the user to interact with the Docker daemon.

* Docker Store - A registry of Docker images, where you can find trusted and enterprise ready containers, plugins, and Docker editions. 

* Official images - sanctioned by Docker; reviewed by a Docker, Inc team; not tied to any company/organization

* User images - images created/shared by users (user may be a person or an organization)

** Cheat sheet

docker --version
docker-compose --version
docker-machine --version

docker run hello-world

docker run -d -p 80:80 --name webserver nginx
  starts a dockerized web server; go to http://localhost/ to see home page

docker ps
  shows you all containers that are running
docker ps -a 
  lists all containers you have run

docker stop webserver
docker start webserver
docker rm -f webserver

docker rmi <image name | id>
  remove an image you no longer need

docker pull <image name>

docker inspect <image name>
  find out more about an image

docker images
  shows all images on your system

** Tutorials

* I started with [Docker for beginners] (https://github.com/docker/labs/tree/master/beginner/)
* More tutorials can be found here: [https://docs.docker.com/samples/](https://docs.docker.com/samples/)



