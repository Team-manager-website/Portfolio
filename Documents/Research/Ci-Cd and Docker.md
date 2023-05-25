# Ci/Cd And Docker

## Intro
In this document I am going to talk about ci/cd. What is ci/cd and what can you do with it. In addition, we will also discuss what docker is and what you can do with it with ci/cd. I am going to talk about the pros and cons and in the and I am giving a little example how I integrated ci/cd into my own project.

## What is ci/cd
Ci is standing for continuous integration and helps the developers to maintain their focus on important things namely writing code. By using ci the do not have to focus on how to integrate code into the existed project. 

Cd is standing for continuous delivery, and it begins when ci stops. Cd simplifies the process to make new code changes to new environments. For example, it can be a production server like Docker. To process the code to a new environment it can automatically build, test and deploy code.

## Pros and consfor using ci/cd
### Pros
* It can automatically build, test and deploy your code what saves you time.
* Faster deployment.
* Get continuously feedback.
* Better code quality.

### Cons
* The pipeline can become to complex and difficult to manage.

## Docker
Docker is a platform that developers can use to build, deploy, run, update and manage applications. It does it by virtualizing the operation system of the computer on which is it installed and running. For example, each computer has a different version of node.js installed and docker ensures that you do not have to convert everything to the right version or install all kinds of things.

## Demo
In my back-end project I have made 2 ci/cd files and I am going to show one of them here so I can explain what is does. Down below you can see the docker-image.yml file from my back-end project. 

 ![image](https://github.com/Team-manager-website/Portfolio/assets/103424907/d80af5d7-a770-42e5-938c-9ea15ea8de78)

At the top of the file, the action is named "Docker Image CI." The workflow is triggered when there is a push event or a pull request to the "master" branch.

The job defined in this workflow is named "build" and it runs on an Ubuntu environment. Here's a breakdown of the steps:

1. The "actions/checkout@v3" step checks out the source code of the project.

2. The "docker/login-action@v2" step logs in to Docker Hub using the provided Docker Hub username and password stored in secrets.

3. The "docker build" step creates a Docker image using the Dockerfile in the current directory. It tags the image as "cedje/teammanager:team."

4. The "docker push" step pushes the built Docker image to the Docker Hub repository "cedje/teammanager:team."

5. The "actions/setup-java@v3" step sets up JDK 11 with the 'temurin' distribution and caches Maven.

6. The "mvn package --file pom.xml" step builds the Maven project by running the "package" goal using the "pom.xml" file.

This workflow automates the process of building a Docker image, pushing it to Docker Hub, and building a Maven project. It ensures that the latest code changes on the "master" branch are built, packaged, and ready for deployment.

## Sources
Elasticweb: https://www.elasticweb.nl/kennisbank/continuous-integration-en-continuous-delivery-verder-uitgelegd <br>
Opsera: https://www.opsera.io/blog/ci-cd-business-benefits <br>
Techtarget: https://www.techtarget.com/searchsoftwarequality/tip/The-pros-and-cons-of-CI-CD-pipelines <br>
medium: https://medium.com/free-code-camp/docker-simplified-96639a35ff36#06d9 
