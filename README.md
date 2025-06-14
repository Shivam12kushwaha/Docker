### Docker is the platform designed to help developers build, share and run container applications.
### Why do we need Dockers?
### Consistency Accross Environments:
**Problem:** Applications often behave differently in developement, testing, and production environments due to variations in configurations, dependecies and infrastructure.\
**Solution:** Docker containers encapsulates all the necessary components, ensuring the application runs consistently accross all environments.
### Isolation:
**Problem:** Running multiple applications on the same host can lead to conflicts such as dependency clashes or resource contention.\
**Solution:** Docker provides isolated environments for each application, preventing interference adn ensuring stable performance.
### Scalability:
**Problem:** Scaling applications to handle increased load can be challenging, requireing manual intervention and configuration.\
**Solution:** Docker make it easy to scale applications horizontally by running multiple container instances allowing for quick and efficient scaling.
### How exactly Docker is used?
![Dockerfile Example](https://media.geeksforgeeks.org/wp-content/uploads/20230419170724/Docker-hub-registry.webp)
### Container/Docker Engine:
Docker Engine is the core component of the Docker platform, responsible for creating, running and managing Docker containers. It serves as the runtime that powers Docker's containization capabilities.\
Here is an in-depth look at the Docker.\
![Dockerfile Example](https://process.filestackapi.com/cache=expiry:max/iP10SKJZQOKeZbtMqTWR)
### Components of Docker Engine:
(1) **Docker Daemon(Dockered):**\
->**Funtion:** The Docker Daemon is the background service running on the host machine. It manages Docker objectssuch as images, containers, networks and volumes.\
->**Interaction:** It listens for Docker API requests and processes them, handling containers life cycle operations like start, stop, restart etc.\
(2) **Docker CLI(Docker):**\
->**Function:** The Docker Command Line Interface is the tool that users interact with to communicate with Docker Daemon.\
->**Usage:** Users run Docker Command through the CLI to perform tasks like building images, running containers and managing Docker resources.\
(3) **REST API:**\
->**Funtion:** The Docker REST API allows communication between the Docker CLI and the Docker Daemon. Iy also enables programmatics interaction with the Docker.\
->**Usage:** Develoopers can use the API to automate Docker operations or integrate Docker functionality into their applications.
### Docker Image:
A Docker Image i a lightweight, stand-alone and executable software package that includes everything needs to run a piece of software, such as the code, runtime, libraries, environments variables and configuration files. Images are used to create Docker Containers, which are instances of these images.
### Components of Docker Image:
1. **Base Image:** The starting point for building an image. It could be a minimal OS image like Alpine, a full-fledged OS like Ubuntu or even another application image like Python or Node.
2. **Application Code:** The actual code and files necessary for the application to run
3. **Dependencies:** Libraries, frameworks and packages required by the application.
4. **Meta Data:** Information about the image such as environment variables, lables and exposed ports.
### Docker Image Life-cycle:
1. **Creation:** Images are created using the docker build command, which processes the instructions in a Docker File to create the image layers.
2. **Storage:** Images are stored locally on the host machine. They can also be pushed and pulled from Docker registeries like DockerHub, AWS ECR, or Google Container Registry.
3. **Distribution:** Images can be stored by pushing them to a Docker registry, allowing others to pull and use the same image.
4. **Execution:** Images are executed by running containers which are instances of these images.
### Docker File:
A Docker file is a text file that contains a series of instructions used to build a Docker image. Each instruction in a Docker File creates a layer in the image, allowing for efficient image creation and reuse of layers. Docker Files are used to automate the image creation process, ensuring consistency and reproducibilty.
### Key components of Docker File:
1. **Base Image(FROM):** Specifies the starting point for the image,which could be a minimal operating system, a specific version of a language runtime or another image example FROM ubuntu:20.04.
2. **Labels(LABEL):** Adds meta data to the image such as version, description or maintainer. Example - LABEL version = '1.0' description = 'My Application'.
3. **Run Command(RUN):** Executes commands in the during the build process, typically used to install software packages. Example: RUN apt-get update & & apt-get install-y python3.
4. **Copy Files(COPY):** Copies files or directories from the host systems to the image. Example: ENV PATH|app|bin:$PATH.
5. **Work Directory(WORKDIR):** Sets the working directory for subsequent instructions. Example: WORKDIR/app.
6. **Expose Ports(EXPOSE):** Informs Docker that the container listens on specified network port. Example: Expose 8080.
7. **Command(CMD):** Provides a default command to run when the container starts. Example: CMD['Python','app.py'].
8. **Volume(VOLUME):** creates a mount point with a specified path and marks it as holding externally mounted volumes from the host or other containers. Example: VOLUME['|data'].
9. **Arguments(ARG):** Defines build-time variables. Example: ARG VERSION=1.0
### Docker Container:
A Docker Container is a lightweight, portable and isolated environment that encapsulatesan application and its dependencies, allowing it to run consistently accross different computing environments. Containers are crreated from Docker images, which are immutable and contain all the necessary components for the application to run.
### Registry:
A Docker Registry is a service that stores and distributes Docker images. It acts as a repository, where users can push, pull and manage Docker Images. DockerHub is the most well-known public registry but private registries can also be set up to securely store and manage images within an Organization.
### Key Components of Docker Registry:
1. **Repositeries:** A Repository is a collection of related Docker images, typically different versions of the same applications. Each repository can hold multiple tags, representing different versions of an image.\
2. **Tags:** tags are used to versions images within a repository. For example, myapp:1.0, myapp:2.0 and myapp:latest are tags for different versions of the my app image.
### Types of Docker Registeries:
1. Docker Hub
2. Private Registeries
3. Third Party Registeries
### Benefits of using Docker Registeries:
1.**Centralized Image Management:** Registeries provide a centralized location to store and manage Docker images, making it easier to organise and distribute them.\
2.**Version Control:** Using Tags, registeries allows version control of images, enabling users to easily roll back to previous versions if needed.\
3.**Collaboration:** Public registries like Docker Hub falicitate collaboration by allowing users to share images with the community or within teams.\
4.**Security:** Private registeries ensure that sensitive images are stored securely and access is controlled within an orgainzation.\
5.**Integration with CI/CD:** Registeries integratte seamlessly with CI/CD pipelines, automating the process of building, storing and deploying Docker images.
### Use Cases:
1. Micro service architecture
2. Continuous Integration and Continuous Deployment
3. Cloud Migration
4. Scalable Web Application
5. testing and QA
6. Machine Learning and AI
7. API Developement and Deployment
### Softwares:
![Dockerfile Example](https://community.aws/_next/image?url=https%3A%2F%2Fassets.community.aws%2Fa%2F2l0avHQeHsb3AR92fLD2c3ccnF9%2Ff62bda7a85b664ef8496d98ee7281b10-jpg.webp%3FimgSize%3D1000x500&w=2048&q=75)
![Dockerfile Example](https://miro.medium.com/v2/resize:fit:728/1*kjZhVc8uPnFOhkxK1Ic9Gg.jpeg)
