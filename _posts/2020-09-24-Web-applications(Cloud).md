---
title: "Web applications and cloud."
layout: post
---

Briefly describe your application, what does it do?
A simple web application which uses an azure database where the database contains a table which consist  Id and a Name the application is used to store names in the cloud database.

Describe the code?

I created a ASP.NET Web App using Visual studio to create my simple web app .
Since I have already created a database in Azure the goal is to create some functions  and  connect the app to Azure database in order to save and get information from - to the database.
I started first by creating a Model class which will represent the information that will be available in the database which looks like this:
![Models](https://github.com/ItsAnass/ItsAnass.github.io/blob/main/assets/Images/W/Models%202021-09-24%20103615.png?raw=true)

I added two razor pages where one page is responsible to add a Name to the database and the other page is responsible to return in a list all the names we have in the database.
This is the page which is responsible to add a Name to our database and it looks like this:
![AddName](https://github.com/ItsAnass/ItsAnass.github.io/blob/main/assets/Images/W/OnPost%202021-09-24%20133800.png?raw=true)
This is the page which is responsible to return all the names we have in a list as shwon below:
![AddName](https://github.com/ItsAnass/ItsAnass.github.io/blob/main/assets/Images/W/ReturnFromDb%202021-09-24%20103953.png?raw=true)
After creating app service in Azure I went to deployment center to connect my repo in order to publish my code and that how was my workflow file looks like:
![WorkFlow](https://github.com/ItsAnass/ItsAnass.github.io/blob/main/assets/Images/W/yml%202021-09-24%20132724.png?raw=true)
And here we can see that the action has been completed and the app is deployed:
![ActionWorkFlow](https://github.com/ItsAnass/ItsAnass.github.io/blob/main/assets/Images/W/Build%20and%20deploy%202021-09-24%20133050.png?raw=true)









