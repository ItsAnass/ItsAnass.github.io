---
title: "Cloud database?"
layout: post
---

## Briefly describe the application, what does it do? And describe the code?

I created a REST API with Azure functions Using SQL, so I used HTTP triggeres type function for these APIs and Visual Studio 2019 to create this mini application.
The application can save names by sending a POST request and by sending a GET request we can get all the names in a list from the database using Azure functions.

![Models](https://github.com/ItsAnass/ItsAnass.github.io/blob/main/assets/Images/Database%20cloud/ModelsClass%202021-09-21%20183319.png?raw=true)

I first created a class for the Models which looks like this.

![CreateFunc](https://github.com/ItsAnass/ItsAnass.github.io/blob/main/assets/Images/Database%20cloud/CreateFunction%202021-09-21%20183438.png?raw=true)
![ReturnDataFunc](https://github.com/ItsAnass/ItsAnass.github.io/blob/main/assets/Images/Database%20cloud/ReturnAllTasksFunction%202021-09-21%20183503.png?raw=true)

Here are my functions which creates and return data from to the database using POST and GET requests.


