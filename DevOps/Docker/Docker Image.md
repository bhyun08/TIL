Docker image is a standardized package that includes all of the files, binaries, libraries, and configurations to run a Docker container. Images are read-only, also known as snapshots, and represent applications and virtual environments at a particular point in time.
# Docker Image Layer
Docker Image is consist of many layer. Docker reads Dockerfile to create a new image layer for each command that changes the file system. Create an image layer only if a change occurs in the file system, rather than creating a layer on every line.
![](https://creboring.net/assets/img/posts/2023-05-29/container-filesystem.jpg)          
When creating an image, rather than making it into a single snapshot, the docker stores it by dividing it into multiple snapshots with multiple layers. 
# UnionFS
To restore and use file system as like many layer, need to system that work layers like file system. What makes this possible is the "Union File System (`UnionFS`)," which plays a key role in the docker image layer. 
![](https://creboring.net/assets/img/posts/2023-05-29/ufstree.jpg)            
UnionFS is system that combines two or more directories as if they were one directory. There is a 'top' and 'bottom' relationship between the two directories, and the contents of the two directories merge like one directory.
# Docker image feature
#### Read-Only System
Docker image is read-only. When container run, file system is provided based on an image. Changes that occur while the container is running are stored in the container's writable layer, and the image is not changed.
### Base Image and Child Image
Docker image can divide base image and child image. Base image is an image that exists independently and not based on other images. For example, images such as `ubuntu` and `alpine` are often used as base images. Child image is an image created by adding a new layer based on the base image. For example, the `python:3.9` image is an image that adds a python environment based on the `ubuntu` image.

---
Reference link 🙂    
https://creboring.net/blog/how-docker-divide-image-layer/       
https://sunrise-min.tistory.com/entry/Docker-Container와-Image란-무엇인가           
https://docs.docker.com/reference/cli/docker/image/ls/             
https://docs.docker.com/get-started/docker-concepts/the-basics/what-is-an-image/ 