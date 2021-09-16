---
title: "What is CI Pipelines?"
layout: post
---

Continuous integration is a set of practices that drive development teams to implement small changes and check in code to version control repositories frequently. Because most modern applications require developing code in different platforms and tools, the team needs a mechanism to integrate and validate its changes.
Moreover, the technical goal of CI is to establish a consistent and automated way to build, package, and test applications. With stability in the integration process in place, teams are more likely to commit code changes more frequently, which leads to better collaboration and software quality.


## How implemented a CI pipeline in GitHub actions on an existing project? And what steps have you gone through? And descrip your GitHub action workflow YAML file.?
![dotnet.CIWorkflow](https://github.com/ItsAnass/s.github.io-/blob/main/assets/Images/CIWorkflow.png?raw=true)
The main thing is to specify the path where the execution has to start.
In my YAML file I used:
* ( on[push]) That means the jobs run every time someone pushes a change to the repository. Its possible also to set up the workflow to only run on certain branches and paths.
* (jobs keyword) Groups together all the jobs that run in my workflow file.
* (name keyword) Is optinal and  it will appear in the Actions tab of the GitHub repository.
* (runs-on keyword) Configures the job to run on an Ubuntu Linux runner.
* (steps keyword) Groups together all the steps that will be done and each item under this section is a separate action .
* (run keyword) Tells the job to execute a command on the runner.
* ( run: dotnet build Source/SpacePark.sln) And here I specified where the code should execute from. 
* (with: dotnet-version: 5.0.x) And ofcourse we have to specify which version of dotnet are we using where I used.



## References

[Github Actions](https://docs.github.com/en/actions/quickstart)

