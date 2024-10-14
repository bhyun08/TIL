Docker demon is one of the components of docker. Docker Demon play a role that docker engine's server. When a user(client) executes a command, the docker daemon handles it and performs a variety of container-related tasks. Specifically, it is responsible for controlling and coordinating the overall behavior of the docker, including image build, container execution and management, networking, and volume management.
![](https://media.geeksforgeeks.org/wp-content/uploads/20240208031606/Screenshot-2024-02-08-031526.png)           
# Docker Demon Feature
1. **Container Management**: Start and stop the container, and monitor its status.
2. **Management Image**: Gets images from Docker Hub or private registry and allows the container to run based on them.
3. **Network Setting**: Manage network settings so containers can communicate with each other.
4. **Management Volume**: Set up and manage storage volumes for data persistence within the container.
5. **Push & Pull images from registry**: If the requested image or container is not already local, the Docker daemon interacts with the Docker registry to import and distribute the requested resources.
6. **Host OS**: It communicates with the kernel of the host operating system to run the container operation.

---
Reference link 🙂    
https://www.geeksforgeeks.org/what-is-docker-daemon/
https://velog.io/@weekbelt/도커데몬Docker-Daemon            
https://junstar92.tistory.com/169