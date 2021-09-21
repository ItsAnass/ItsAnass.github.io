---
title: "Cloud database?"
layout: post
---

## Briefly describe the application, what does it do? And describe the code? And describe the database?

I created a REST API with Azure functions Using SQL, so I used HTTP triggeres type function for these APIs and Visual Studio 2019 to create this mini application.
The application can save names by sending a POST request and by sending a GET request we can get all the names in a list from the database using Azure functions.

I first created a class for the Models which looks like this:

![Models](https://github.com/ItsAnass/ItsAnass.github.io/blob/main/assets/Images/Database%20cloud/ModelsClass%202021-09-21%20183319.png?raw=true)

Here are my functions which creates and return data from to the database using POST and GET requests.

![CreateFunc](https://github.com/ItsAnass/ItsAnass.github.io/blob/main/assets/Images/Database%20cloud/CreateFunction%202021-09-21%20183438.png?raw=true)
![ReturnDataFunc](https://github.com/ItsAnass/ItsAnass.github.io/blob/main/assets/Images/Database%20cloud/ReturnAllTasksFunction%202021-09-21%20183503.png?raw=true)


For the database I created a new database in Azure then I had to create a table inside the database. For that, I need to add the current machine IP Address to Firewall Settings in our Azure database.
Now we need a table in our database for data storing to do that I went to Query Editor and I wrote this query in order to add the first table:

![ReturnDataFunc](https://github.com/ItsAnass/ItsAnass.github.io/blob/main/assets/Images/Database%20cloud/Database_Query%202021-09-21%20183831.png?raw=true)


Then I fixed the database connection so I have the right server credentials and they looked like this:
![ReturnDataFunc](https://github.com/ItsAnass/ItsAnass.github.io/blob/main/assets/Images/Database%20cloud/JsonFile%202021-09-21%20183231.png?raw=true)

I used PostMan app to test my requests and that is the result:

![ReturnData](https://github.com/ItsAnass/ItsAnass.github.io/blob/main/assets/Images/Database%20cloud/PostManRetu%202021-09-21%20192238.png?raw=true)





