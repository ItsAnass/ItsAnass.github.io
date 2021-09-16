---
title: "Containers and dockers (GitHub)."
layout: post
---

## What has been installed locally / Github?

First of all I didn't need to install any thing since I have already installed Docker Desktop and GitHub Desktop.
I started by forking the project from the given link and started working on it by adding the required files.



## How did you get the application to run in a container and describe your docker file?

I added a folder which contains docker file and by using the windows terminal I located the file path and then I typed (docker build .).
The windows terminal will go through the docker file and it wil create a container according to the information in the docker file.

![DockerFile](https://github.com/ItsAnass/s.github.io-/blob/main/assets/Images/DockerfileScreen.png?raw=true)
  

* Line 6 shows (FROM) It creates a layer from the aspnet:3.1  Docker image.
* Line 7 (WORKDIR ) This command is used to define the working directory of a Docker container at any given time and
if the (WORKDIR) Command is not written in the Dockerfile, it will automatically be created by the Docker compiler.
* Line 8-9 (EXPOSE) The instruction exposes a particular port with a specified protocol inside a Docker Container.
* Line 13 (COPY)  It let you copy files from a specific location into a Docker image.
* Line 14 (RUN ) Lets you execute commands inside of your Docker image.
* Line 25 (ENTRYPOINT) Allows you to configure a container that will run as an executable.

## Describe your github pipeline?

![CI](https://github.com/ItsAnass/s.github.io-/blob/main/assets/Images/DockerfileScreen.png?raw=true)

I have explained earlier about the basics of the github pipeline file.
I will start with the new jobs that I added to the file.
In line 10 ( docker meta ) I used a GitHub Action to extract metadata from Git reference and GitHub events. This action is particularly useful if used with Docker Build Push action to tag and label Docker images.
In line 19 ( setup-qemu )  The action can be useful if you want to add emulation support with QEMU to be able to build against more platforms.
Line 22 ( setup-buildx ) the action will create and boot a builder using by default the docker-container builder driver.
Line 25 ( login ) Action will take care to log in against a Docker registry.
Line 32 and 38 (build/push) We are building the image and then we are pushing it to the repository with the help of the dockerfile that we already have.



## References

[Docker tag, extended description](https://docs.docker.com/engine/reference/commandline/tag/)

[About the Github token](https://docs.github.com/en/actions/reference/authentication-in-a-workflow)

[Github Docker build-push](https://github.com/docker/buildx/blob/master/docs/reference/buildx_build.md#push)

[Github, build-push-action](https://github.com/docker/build-push-action)

[Github, login-action](https://github.com/docker/login-action#github-container-registry)

[What's wrong with the docker: latest tag?](https://vsupalov.com/docker-latest-tag/)
