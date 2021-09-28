---
title: "Serverless and Function As A Service (FaaS)?"
layout: post
---

Function as a Service (FaaS) and serverless are two such technologies that approached the forefront due to the popularity of cloud computing. Both these technologies aim to:
* Provide cost-effective cloud platforms.
* Eliminate the need for infrastructure management.
 Sometimes the terms FaaS and serverless are used interchangeably.However, they are two different technologies with some significant differences.
 
 Serverless.
 
Serverless is a computing model where infrastructure orchestration is managed by service providers.However, even with these cloud servers, the management and configuration     tasks of the cloud infrastructure were left to the users.
This is where serverless comes into play. Moreover, serverless aims to eliminate the management and configuration tasks enabling users to solely focus on the application.
This is not limited solely to server instances but extends to other areas, too, such as:
* Serverless databases.
* DevOps pipelines. 

Function as a Service.

Apart of that, function as a service is a relatively newer concept that aims to offer developers the freedom to create software functions in a cloud environment easily. In this method, the developers will still create the application logic, yet the code is executed in stateless compute instances that are managed by the cloud provider.

How did you get it to run in Azure functions?

![dotnet.Code](https://github.com/ItsAnass/ItsAnass.github.io/blob/main/assets/Images/MiniCalcCode.png?raw=true)

Here how my code looks like where I created a static async Task method where it returns an object result.

How did you test the application?

![dotnet.Code](https://github.com/ItsAnass/ItsAnass.github.io/blob/main/assets/Images/CodeTest.png?raw=true)

The code was tested by using the query string which sends an HTTP request, where I wrote 2 different values as shown in the above image.

![dotnet.Code](https://github.com/ItsAnass/ItsAnass.github.io/blob/main/assets/Images/TestCodeOutput.png?raw=true)

The above  image here shows the output of my HTTP request and the total number of the 2 values I enterd.







