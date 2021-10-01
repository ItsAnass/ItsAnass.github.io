---
title: "Files in the cloud."
layout: post
---
Describe the application, what does it do?

A simple application where I can upload, view and delete images using Azure Blob Storage.







## Create a diagram that shows how the data flows?
![DataFlow](https://github.com/ItsAnass/ItsAnass.github.io/blob/main/assets/Images/Untitled%20Diagram.png?raw=true)

## Describe the code?
First of all I created a storage account in Azure then I downloaded Azure storage explorer which looks like this:
![StorageExp](https://github.com/ItsAnass/ItsAnass.github.io/blob/main/assets/Images/Blobs/Storage%20Exp%202021-10-01%20134825.png?raw=true)

I then connected my storage account explorer to Azure account using access keys which looks like this:
![AccessKeys](https://github.com/ItsAnass/ItsAnass.github.io/blob/main/assets/Images/Blobs/Connection%20string%202021-10-01%20135316.png?raw=true)

I then created a ASP.NET Web App then I added some methods to the my HomeController class which will be responsible to upload, view and delete the images the methods are :
![Methods](https://github.com/ItsAnass/ItsAnass.github.io/blob/main/assets/Images/Blobs/Index%202021-10-01%20142210.png?raw=true)

* From line 31 it retrieves storage account information from the connection string.
* From line 34 it creates a blob client for interacting with the blob service.
* In Line 38 to view the uploaded blob in a browser, we have two options. The first option is to use a Shared Access Signature (SAS) token to delegate access to the resource or we can set permissions to allow public access to blobs in this container.
* Line 40 gets all Cloud Block Blobs in the blobContainerName and passes them to teh view.







