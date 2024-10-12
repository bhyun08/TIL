Dockerfile is a file that to make [[Docker Image]]. Docker Image is created with syntax written in the file, and the created image can be executed in a container.
![](https://media.geeksforgeeks.org/wp-content/uploads/20230406105935/dockerfile-2.png)         
# Dockerfile Command 
| Keyword      | Discription                                                                         |
| ------------ | ----------------------------------------------------------------------------------- |
| `#`          | annotation                                                                          |
| `FROM`       | Designate docker base image                                                         |
| `MAINTAINER` | Name and information of the person who created the image                            |
| `LABEL`      | Metadata written in Key-value format                                                |
| `RUN`        | Execute Commands for Container Build                                                |
| `COPY`       | Copy host OS's file when you build the container                                    |
| `ADD`        | Copy the host's (tar, url) during container build                                   |
| `WORKDIR`    | Working directory in which the command will be executed when the container is built |
| `ENV`        | Environmental Variables                                                             |
| `USER`       | User settings to apply when executing commands and containers (default: root)       |
| `VOLUME`     | Mounting a specific directory within a container to a path outside the container    |
| `EXPOSE`     | Specify the port to use externally when operating the container                     |
| `CMD`        | Specify services and scripts to run automatically when the container operates       |
| `ENTRYPOINT` | Used with CMD when specifying Commands                                              |
# Dockerfile build
1. Write Docker file that define the environment in which the application will run and the required packages, etc.
2. Docker image build with `docker build` command based on dockerfile.
``` bash
docker build -t myapp:latest .
```
3. Run the container using the built image.
```bash
docker run -d -p 8080:8080 myapp:latest
```

---
Reference link 🙂    
https://www.cloudbees.com/blog/what-is-a-dockerfile         
https://stack94.tistory.com/entry/docker-도커-파일Dockerfile의-문법-및-작성-예시        
https://docs.docker.com/reference/dockerfile/          
https://www.geeksforgeeks.org/what-is-dockerfile/         