Docker is open source software platform that help applications run in a virtualized environment called containers and can builds, tests and develops fast. Dockers allow applications and their execution environments (such as required libraries, settings, etc.) to run consistently anywhere in a single package.
# How to work Docker?
![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*uuZ-h5EH76LOtJ614z-qDA.png)                
1. First, to run you application in docker, you have to write Dockerfile.
2. Build a Docker image based on Dockerfile using a build tool, such as Docker CLI or Docker Compose, or a CI/CD system.
3. Docker images allow you to create and run Docker containers, which are instances of Docker images that can be started, stopped, and managed independently.
4. You can view running containers, stop containers, start stopped containers, and remove containers when they are no longer needed.
5. Docker images can be posted to a registry, such as Docker Hub or a private registry. Posting an image allows others to use it or distribute it to a different environment. You can also distribute the image by sharing a Docker image file or pushing it to a version control system.
6. Continue to develop and improve applications, update Dockerfile and rebuild images to repeat Docker images.
# Docker Pros
#### Environmental consistency
Dockers allow applications to run using the same image in development, testing, and production environments. This protect the situation that "It works well on my computer 😣".
#### Portability
Docker containers operate consistently across a variety of operating systems.
#### Automation and CI/CD
Integration into the CI/CD pipeline allows code changes to be automatically built and distributed as container images.

---
Reference link 🙂    
https://aws.amazon.com/ko/docker/             
https://velog.io/@markany/도커에-대한-어떤-것-1.-도커란-무엇인가              
https://medium.com/@augustineozor/docker-workflow-b9fe71d32184