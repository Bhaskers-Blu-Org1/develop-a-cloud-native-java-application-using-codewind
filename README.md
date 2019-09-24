## Work in progress

# develop-a-cloud-native-java-application-using-codewind
This tutorial provides steps to create a cloud native java application using Codewind

## Overview

Eclipse Codewind is an open source project that makes it easier for developers to create cloud-native applications within their favorite IDE. As of now, Codewind supports Visual Studio Code, Eclipse IDE and Eclipse Che. More editors will be added in the coming months.

In this tutorial, we will provide steps to develop a java application using Codewind installed over Eclipse IDE.

Codewind enables you to create applications from templates and provide support for launching, updating, testing, and debugging in Docker containers on the desktop. Codewind also supports these features on Kubernetes. You can use Codewind to move existing applications to Docker and Kuberenetes. Codewind provides validation to ensure that applications follow best practices.

Codewind helps you in building high-quality cloud-native applications for Kubernetes, regardless of your IDE or language.

Let's start with installing Codewind on Eclipse IDE.


## Installing Codewind for Eclipse

Prerequisites:
- Download and install the latest [Eclipse IDE for Java EE Developers](https://www.eclipse.org/downloads/packages/release/) or use an existing installation. The earliest supported version of the Eclipse IDE for Codewind for Eclipse is 4.11.0 (2019-03).
- Install [Docker](https://docs.docker.com/install/)

Complete the installation:
1. Open the Eclipse IDE and navigate to Help > Eclipse Marketplace.
2. Search for Codewind.
3. Click the Install button.
4. Finish the wizard and accept licenses as needed.
5. When the installation is complete, restart Eclipse.
6. In Eclipse, navigate to Window -> Show View -> Other.... -> Codewind -> Codewind Explorer.
7. Codewind requires the installation of additional Docker images to run. Double-click on the Codewind item in the Codewind Explorer view to complete the installation. The installation may take a few minutes to complete.
8. Codewind creates a folder called codewind-workspace within your home directory (~/codewind-workspace on mac) to contain your projects.


## TODO to cover Codewind for VS Code?

## Types of templates and their overview

Codewind has a default set of templates available from which you can create a project. By default the following templates are supported, as of now and more templates will be added - **Go**, **Lagom Java**, **Node.js Express**, **Open Liberty**, **Python**, **Sprint Boot**, **Swift**, **WebSphere Liberty Microprofile**
TODO need an image here?
You can create your own template and use it to create a project. More details [Here](https://www.eclipse.org/codewind/mdteclipseusingadifferenttemplate.html).


### code-wind workspace is not tied to an editor. Any editor can be used

## Create and run a microprofile project
Let us create a project using **WebSphere Liberty Microprofile** template.
1. In the Codewind Explorer view, ensure that Codewind is running. Or else bouble click COdewind item to start.
2. Upon start, expand `Codewind` item and right click on `Local Projects` and click `New Project....`.
3. Enter a name for the project and select `WebSphere Liberty MicroProfile` under templates. Click `Finish` to create the project.
4. The project is built, deployed and started. 
5. Each project shows the application status and the build status. A context menu on each project enables you to open your application in a browser, view application and build logs, restart in debug mode, and much more. Refer to [this link](https://www.eclipse.org/codewind/mdteclipsemanagingprojects.html) for the list of context menu items and their functionality.
6. In Codewind Explorer view, right click on the project that was created in above step, and click `Open Application`. This opens the application in the default Eclipse browser. You can start using the application.

TODO-Organize It is very easy to make the changes and deploy them. Let us modify Example.java file. Before making modification, check the response for http://localhost:<port>/v1/example, in a browser. Now, let us modify and change the display message to "Congratulations, your modified application is up and running!!!". Save the file. Wait for a few moments for the changes to be built and deployed. Now check by invoking the rest api http://localhost:<port>/v1/example. The modified message should be displayed. It is this easy to modify changes in a cloud native application. 
  
You can then go on to modify this application to add your business logic. This way you focus on just what is needed. All other aspects are taken care of, 



## Explain directory structure

## Run the application using Codewind

## Access the application

## Debugging in Codewind
TODO https://www.eclipse.org/codewind/troubleshooting.html

## TODO Uninstalling Codewind from eclipse? https://www.eclipse.org/codewind/mdteclipseuninstall.html
