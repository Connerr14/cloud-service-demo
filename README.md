Project Name: Cloud-service-demo
Purpose: To utilize git and github and to show an example of what could be hosted in the cloud.
Files included: index.html, README.md
Version control helps a cloud project because it keeps the version history of the project and allows for roll-backs to different versions.

Lab Assignment 2 Questions:

Question: Explain the difference between a Docker image and a Docker container in your
own words. Suggested length: 2–3 sentences.
The difference between a Docker image and a Docker container is that a Docker image is what defines the blueprint of how a container runs and the environment that its in and a Docker container is a Docker image instance. Docker images are static, whilst a docker container is constructed following the static instructions of the image and proceeds to be a active running instance of the image.


1. What docker is: 
Docker is a operating system level virtualization platform. It allows applications to share
the host operating system kernel instead of running a separate guest os. This design allows for fast, lightweight,
and portable containers that are isolated from each other.

2. What a docker image is:
A docker image is a static template that contains instructions for creating a docker container. It can contain application code, libraries, and dependencies. It serves as the blueprint for creating containers.


3. What a docker container is:
A docker container is a standard unit of software that packages up code and all its dependencies so the application runs
quickly and reliably from one environment to another. It is a lightweight, standalone, executable package of software that includes everything that is needed to run a application. More specifically, it is a runnable instance of a Docker image.

4. How to build and run your application using Docker:
Firstly, you need to have a valid Dockerfile saved in the working directory. In the Dockerfile, you write a series of instructions from top to bottom that tell Docker how to assemble the environment. Then you need to build the Docker image. You can build the docker image by using the build command. The -t flag tags your image with a name and version, and the trailing . tells Docker to look for the Dockerfile in the current directory. For example, the following command will build a docker image: docker build -t cloud-service-demo:1.0 .
Next, you need to run the Docker container from your newly created image using the run command. The run command allows you to also assign a name to the running container instance, whether it runs in detached mode, and where to port forward from/to and more. For example, the following command can be ran to run a container in detached mode, with name cloud-demo-container, and forwarding port 8080 on the local machine to port 80 in the container: docker run -d --name cloud-demo-container -p 8080:80 cloud-service-demo:1.0
Next, you can verify a container is running by running the command "docker ps" to check for active containers.
Lastly, you can access and test your application by opening a web browser and utilizing localhost with the port that was used.