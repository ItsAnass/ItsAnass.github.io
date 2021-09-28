---
title: "Containers and dockers (GitHub)."
layout: post
---

What has been installed locally / Github?

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

![CI](https://github.com/ItsAnass/s.github.io-/blob/main/assets/Images/CI.png?raw=true)

* ( on[push]) That means the jobs run every time someone pushes a change to the repository. Its possible also to set up the workflow to only run on certain branches and paths.
* (jobs keyword) Groups together all the jobs that run in my workflow file.
* (name keyword) Is optinal and it will appear in the Actions tab of the GitHub repository.
* (runs-on keyword) Configures the job to run on an Ubuntu Linux runner.
* (steps keyword) Groups together all the steps that will be done and each item under this section is a separate action .
* (run keyword) Tells the job to execute a command on the runner.
* Line 10 ( docker meta ) I used a GitHub Action to extract metadata from Git reference and GitHub events. This action is particularly useful if used with Docker Build Push action to tag and label Docker images.
* Line 19 ( setup-qemu )  The action can be useful if you want to add emulation support with QEMU to be able to build against more platforms.
* Line 22 ( setup-buildx ) the action will create and boot a builder using by default the docker-container builder driver.
* Line 25 ( login ) Action will take care to log in against a Docker registry.
* Line 32 and 38 (build/push) We are building the image and then we are pushing it to the repository with the help of the dockerfile that we already have.



## References

[Working with the Container registry](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry)


