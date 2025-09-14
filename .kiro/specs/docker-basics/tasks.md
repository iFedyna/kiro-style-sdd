# Learning Plan: Docker Basics

- [ ] 1. Understanding Docker Fundamentals and Containerization
  - **Action:** Explain what Docker is, the concept of containerization, and how containers differ from virtual machines using the apartment building analogy. Create an exercise asking the user to list 3 key benefits of using containers over traditional deployment methods. Verify the user identifies benefits like portability, consistency, and isolation.
  - _Requirements: 1.1, 1.2, 1.3_

- [ ] 2. Installing and Setting Up Docker
  - **Action:** Explain the Docker installation process for the user's operating system (Windows, macOS, or Linux) and common installation challenges. Create an exercise asking the user to install Docker and run `docker --version` to verify the installation. Verify the user can successfully run Docker commands and see version information.
  - _Requirements: 2.1, 2.2, 2.3_

- [ ] 3. Running Your First Container
  - **Action:** Explain the basic `docker run` command and what happens when you run a container. Create an exercise asking the user to run `docker run hello-world` and explain what they observe. Verify the user understands the pull and execution process.
  - _Requirements: 3.1_

- [ ] 4. Managing Container Lifecycle
  - [ ] 4.1 Listing and Managing Running Containers
    - **Action:** Explain `docker ps` for listing running containers and `docker stop` for stopping containers. Create an exercise asking the user to run an nginx container in the background, list it, then stop it. Verify the user can successfully manage the container lifecycle.
    - _Requirements: 3.2, 3.3_
  
  - [ ] 4.2 Working with All Containers (Including Stopped)
    - **Action:** Explain `docker ps -a` to view all containers and `docker rm` to remove containers. Create an exercise asking the user to list all containers and remove any stopped ones. Verify the user can clean up unused containers properly.
    - _Requirements: 3.4, 3.5_

- [ ] 5. Working with Docker Images
  - [ ] 5.1 Pulling and Listing Images
    - **Action:** Explain Docker images as templates for containers and the concept of Docker Hub. Create an exercise asking the user to pull an Ubuntu image and list all local images using `docker images`. Verify the user can successfully pull and list images.
    - _Requirements: 4.1, 4.2_
  
  - [ ] 5.2 Removing Images
    - **Action:** Explain when and how to remove Docker images using `docker rmi`. Create an exercise asking the user to remove an unused image. Verify the user can safely remove images without affecting running containers.
    - _Requirements: 4.3_

- [ ] 6. Understanding the Dockerfile Structure
  - **Action:** Explain what a Dockerfile is and its basic structure including FROM, RUN, COPY, WORKDIR, and CMD instructions. Create an exercise asking the user to create a simple Dockerfile for a basic "Hello World" application. Verify the Dockerfile has proper syntax and includes the essential instructions.
  - _Requirements: 5.1, 5.2_

- [ ] 7. Building Custom Images
  - **Action:** Explain the `docker build` command and the build process. Create an exercise asking the user to build an image from their Dockerfile and run a container from it. Verify the user can successfully build and run their custom image.
  - _Requirements: 5.3, 4.4_

- [ ] 8. Data Persistence with Volumes
  - **Action:** Explain the ephemeral nature of containers and the need for persistent data using volumes. Create an exercise asking the user to create a named volume and run a container that uses it. Verify the user understands how data persists across container restarts.
  - _Requirements: 6.1_

- [ ] 9. Working with Bind Mounts
  - **Action:** Explain bind mounts for sharing host files with containers and their development use cases. Create an exercise asking the user to run a container with a bind mount to share a local file. Verify the user can successfully share files between host and container.
  - _Requirements: 6.2, 6.3_

- [ ] 10. Basic Container Networking
  - **Action:** Explain container networking concepts and port exposure using the `-p` flag. Create an exercise asking the user to run a web server container and expose its port to access it from the host. Verify the user can access the containerized service from their host machine.
  - _Requirements: 7.1_

- [ ] 11. Multi-Container Applications with Docker Compose
  - **Action:** Introduce Docker Compose for managing multi-container applications and the docker-compose.yml file structure. Create an exercise asking the user to create a simple docker-compose.yml file with two services (e.g., web app and database). Verify the docker-compose.yml file is properly structured and defines the services.
  - _Requirements: 8.1_

- [ ] 12. Managing Application Lifecycle with Docker Compose
  - **Action:** Explain `docker-compose up` and `docker-compose down` commands. Create an exercise asking the user to start their multi-container application and then stop it. Verify the user can properly start and stop multi-container applications.
  - _Requirements: 8.2, 8.3_

- [ ] 13. Troubleshooting Common Issues
  - **Action:** Explain common Docker problems and troubleshooting techniques using `docker logs` and `docker stats`. Create an exercise asking the user to intentionally create a failing container and debug it using logs. Verify the user can identify and resolve common container issues.
  - _Requirements: 9.1, 9.2_

- [ ] 14. Docker Best Practices
  - **Action:** Explain Docker best practices including image optimization, security, and resource management. Create an exercise asking the user to review and optimize a poorly designed Dockerfile. Verify the user can identify and apply optimization techniques.
  - _Requirements: 9.3_

- [ ] 15. Capstone Project: Containerizing a Simple Web Application
  - **Action:** Guide the user through creating a complete Docker setup for a simple web application including Dockerfile, docker-compose.yml, volumes, and proper networking. Create an exercise asking the user to containerize a basic Flask/Express application. Verify the final application works correctly in containers and follows best practices.
  - _Requirements: All previous concepts_