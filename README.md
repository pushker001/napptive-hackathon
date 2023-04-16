
# Owncloud

OwnCloud is a self-hosted cloud storage solution that allows you to store, share and synchronize your files and documents securely. 

## How to use OwnCloud
- First, make sure you have a web server, PHP, and a database management system installed.
- Download OwnCloud from their website and extract it to a folder on your web server.
- Create a new database and user for OwnCloud.
- Open your web browser, go to the OwnCloud URL, and follow the installation instructions.
- To upload files, log in to OwnCloud and click "Upload" to select and upload files.
- To share files, click "Share" next to the file, enter the email of the person you want to share with, and click "Send".
- To synchronize files, download and install the OwnCloud desktop client, log in, select the files to sync, and click "Sync".

## How to Deploy OwnCLoud on NAPPTIVE PLAYGROUND 

Before Deploying the application on NAPPTIVE first we need to create an OAM file(Open Application model) for doing this we need to create a YAML file in which we can add the component and properties required to migrate the application in OAM.

![Screenshot (342)](https://user-images.githubusercontent.com/50774898/232184967-03b23bed-3e3f-4b33-8afc-cd35cdad9283.png)

A Component represents a single microservice from the Application. To define it, select the type of component that adapts best to the use case, and define its properties. here I have choose webservice(Describes long-running, scalable, containerized services that have a stable network endpoint to receive external network traffic from customers) 

## Traits
A Trait represents an extension for an application component. This facilitates reusing components in different situations, and simplifies their packaging as the developer does not need to add any extra information for its deployment. For example, exposing an application component to the public Internet can be easily done by attaching an ingress trait. The trait offers the same abstraction as the component and will create the underlying ingress attending to the installed controller and cloud provider. In this way, the developer can publish the component with its parameters, and when creating the application, the ingress can be easily added. Other examples of traits include mounting volumes, adding labels, exporting logs, exploring monitoring information, etc.
In my case I used napptive-ingress(Expose a component to the outside with a K8s ingress)

![Screenshot (344)](https://user-images.githubusercontent.com/50774898/232185365-863e9c6e-7ef2-4a03-a4bd-ecb672be82b7.png)

After you've completed all of this, upload the yaml file to the NAPPTIVE platform and click the Deploy button. 

![Screenshot (345)](https://user-images.githubusercontent.com/50774898/232186941-fe8c4ec3-3eff-46cf-89a9-8640c7aa6148.png)


Finally, you can see on the screen that your application is running.


![Screenshot (346)](https://user-images.githubusercontent.com/50774898/232187050-36521c1b-f8ef-41a0-9daf-ae7546e63b62.png)
