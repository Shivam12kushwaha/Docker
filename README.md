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
