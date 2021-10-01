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

I then created a ASP.NET Web App then I added some methods to the my HomeController class which will be responsible to upload, view and delete the images starting with Index method :
![Methods](https://github.com/ItsAnass/ItsAnass.github.io/blob/main/assets/Images/Blobs/Index%202021-10-01%20142210.png?raw=true)

* From line 31 it retrieves storage account information from the connection string.
* From line 34 it creates a blob client for interacting with the blob service.
* In Line 38 to view the uploaded blob in a browser, we have two options. The first option is to use a Shared Access Signature (SAS) token to delegate access to the resource or we can set permissions to allow public access to blobs in this container.
* Line 40 gets all Cloud Block Blobs in the blobContainerName and passes them to teh view.

![Methods](https://github.com/ItsAnass/ItsAnass.github.io/blob/main/assets/Images/Blobs/Uploadmethod2021-10-01%20144309.png?raw=true)

As we can see in the UploadAsync method we have a for loop which loops throgh the selected files and upload them to our blob.

![Methods](https://github.com/ItsAnass/ItsAnass.github.io/blob/main/assets/Images/Blobs/Delete%202021-10-01%20144513.png?raw=true)

Here is the delete method which takes a string parameter and this string will be the URI of the image so that it can be deleted from the blob. 

Here how I connected my application to Azure storage :

![Methods](https://github.com/ItsAnass/ItsAnass.github.io/blob/main/assets/Images/Blobs/Screenshdddot%202021-10-01%20150838.png?raw=true)

In local, it will read the local storage account like "UseDevelopmentStorage=true".
When you publish to Azure, it will use your webapp's MSI to get the connectionstring from key vault.

Starting with my Index.cshtml file this is how I managed between calling the methods according to the user selection:

![Methods](https://github.com/ItsAnass/ItsAnass.github.io/blob/main/assets/Images/Blobs/Screenshot%202021-10-01%20150807.png?raw=true)

Line 29-35 displays a 'Select Files' button that uses a File Upload control to select files to be uploaded and
calls the JS function: DisplayFilesToUpload() that lists the file name and size for all files to be uploaded.
Also the JS function displays the Upload submit button that calls UploadAsync that uploads the files to Azure Blob Storage.

![Methods](https://github.com/ItsAnass/ItsAnass.github.io/blob/main/assets/Images/Blobs/Screenshot%202021-10-01%20150838.png?raw=true)

Line 44-59 loops through all files and displays two items:
* The Image 
* A delete icon that calls deleteImage JS function

![Methods](https://github.com/ItsAnass/ItsAnass.github.io/blob/main/assets/Images/Blobs/Screenshot%202021-10-01%20150907dd.png?raw=true)

Two script functions:
* First one calls async Task<ActionResult> DeleteImage(string name) in the HomeController and Refreshes the page.
* Second one lists the file name and size for all files to be uploaded by updating the <p id="FilesToUpload"></p> control.

Thats how it looks when I have uploaded one image:
  
![Methods](https://github.com/ItsAnass/ItsAnass.github.io/blob/main/assets/Images/Blobs/Screenshot%202021-10-01%20154212.png?raw=true)
  
  
  

  
  
## Explain with your own words what Microsoft does to secure your blob data?
  
Microsoft uses encrypted 256-bit AES encryption but we still have the option to either use Microsoft manage encryption keys or we can use our own keys with customer-managed keys stored in Azure Key Vault.
  










