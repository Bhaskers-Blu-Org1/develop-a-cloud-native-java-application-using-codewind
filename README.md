## Work in progress

# develop-a-cloud-native-java-application-using-codewind
This tutorial provides steps to create a cloud native java application using Codewind

## Overview

Eclipse Codewind is an open source project that makes it easier for developers to create cloud-native applications within their favorite IDE. As of now, Codewind supports Visual Studio Code, Eclipse IDE and Eclipse Che. More editors will be added in the coming months.

In this tutorial, we will provide steps to develop a java application using Codewind installed over *Eclipse IDE*.

Codewind enables you to create applications from templates and provide support for launching, updating, testing, and debugging in Docker containers on the desktop. Codewind also supports these features on Kubernetes. You can use Codewind to move existing applications to Docker and Kuberenetes. Codewind provides validation to ensure that applications follow best practices.

Codewind helps you in building high-quality cloud-native applications for Kubernetes, regardless of your IDE or language.

Let's start with installing Codewind on Eclipse IDE.


## Installing Codewind for Eclipse

Prerequisites:
- Download and install the latest [Eclipse IDE for Java EE Developers](https://www.eclipse.org/downloads/packages/release/) or use an existing installation. Eclipse IDE version 4.11.0 onwards support Codewind. 
- Install [Docker](https://docs.docker.com/install/)

Complete the installation:
1. Open the Eclipse IDE and navigate to Help > Eclipse Marketplace.
2. Search for Codewind.
3. Click the Install button.
4. Finish the wizard and accept licenses as needed.
TODO: add gif here.. There is some error on eclipse
5. When the installation is complete, restart Eclipse.
6. In Eclipse, navigate to Window -> Show View -> Other.... -> Codewind -> Codewind Explorer.
7. Codewind requires the installation of additional Docker images to run. Double-click on the Codewind item in the Codewind Explorer view to complete the installation. The installation may take a few minutes to complete.
8. Codewind creates a folder called codewind-workspace within your home directory (~/codewind-workspace on mac) to contain your projects.

>> This `codewind-workspace` can be accessed across editors. If you have created Codewind projects in Eclipse IDE, then those projects can be accessed from Visual Studio code's Codewind plugin because of the codewind-workspace folder that is compatible across editors.


## TODO to cover Codewind for VS Code/Eclipse Che/Command line?

## Types of templates and their overview

Codewind provides a set of templates available from which you can create a project. By default the following templates are supported, as of now and more templates will be added - **Go**, **Lagom Java**, **Node.js Express**, **Open Liberty**, **Python**, **Sprint Boot**, **Swift**, **WebSphere Liberty Microprofile**
TODO need an image here?
You can create your own template and use it to create a project. More details [Here](https://www.eclipse.org/codewind/mdteclipseusingadifferenttemplate.html).


## Create and run a microprofile project
In this tutorial, let us create a project using **WebSphere Liberty Microprofile** template available in Codewind.
1. In the Codewind Explorer view, ensure that Codewind is running. If not, double click Codewind item to start Codewind.
2. Upon start, expand `Codewind` item and right click on `Local Projects` and click `New Project....`.
3. Enter a name for the project and select `WebSphere Liberty MicroProfile` under templates. Click `Finish` to create the project. Note that `Dockerfile` and `pom.xml` are created with the necessary entries.
![Project Structure](./images/project-structure.png)
You can edit files to suit your needs.
4. A new project is created with all the required directories and files for cloud native java application.
5. The project gets built, deployed and started.
6. A context menu on the project enables you to open your application in a browser, view application and build logs, restart in debug mode, and much more. Refer to [this link](https://www.eclipse.org/codewind/mdteclipsemanagingprojects.html) for the list of context menu items and their functionality.
7. In Codewind Explorer view, right click on the project that was created in above step, and click `Open Application`. This opens the application in the default Eclipse browser. You can start using the application.


Modifying the application:

It is very easy to make the changes and deploy them. Let us modify Example.java file. Before making modification, check the response for http://localhost:<port>/v1/example, in a browser (get port number from the home page of the application). Now, let us modify and change the display message to `Congratulations, your modified application is up and running!!!`. Save the file. Wait for a few moments for the changes to be built and deployed. Now check by invoking the rest api http://localhost:<port>/v1/example on your browser. The modified message should be displayed. It is this easy to modify changes in a cloud native application. 

You can then go on to modify this application to add your business logic. This way you focus on just what is needed for the business logic and not worry about other environmental issues while building a cloud native application. 



## Debugging in Codewind
Check Debugging Codewind projects [here](https://www.eclipse.org/codewind/mdteclipsedebugproject.html)

Check troubleshooting guidelines for Codewind [here](https://www.eclipse.org/codewind/troubleshooting.html)

## Uninstalling Codewind from eclipse?

https://www.eclipse.org/codewind/mdteclipseuninstall.html
