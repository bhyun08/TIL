Docker Registry is central storage that save and distribute [[Docker Image]]. Namely, Docker Registry is a system used to store container images and to download or upload them when needed. Docker registry help to share or distribute image in various develop environment.
![](https://blog.kakaocdn.net/dn/bNGzFh/btqVbu7hXi9/2hnHm5S8QP4cCNg4cg5sF1/img.png)          
Docker registry worked by docker demon. Docker demon pull or push on Docker Registry.
# Docker Repository
Docker Repository is unit of docker registry. Each Docker image save on Repository. One repository can store multiple versions (tags) for the same application or service.
# Docker Hub
It's the most well-known **public registry**. It's accessible to anyone, basically, Docker setting to download and upload Docker image through Docker hub.
# Private Registry
Instead of a publicly accessible registry like Docker Hub, you can also set up a private registry that is managed in-house, which allows you to keep images that are only used within your company or protect sensitive data. You can install and use Docker Registry provided by Docker directly, or use managed registers based on the cloud, such as `Amazon Elastic Container Registry (ECR)` on AWS, `Azure Container Registry`, and `Google Container Registry`.
# Pull & Push
- **Push**: Developers upload local or build images to the registry.
- **Pull**: Image can be downloaded (pulled) by another user or system, typically used to deploy an application. 

**Way to push and pull images.**

Push:
```bash
docker push username/repository:tag
```

Pull:
```bash
docker pull username/repository:tag
```

---
Reference link 🙂    
https://www.aquasec.com/cloud-native-academy/docker-container/docker-registry/#:~:text=A%20Docker%20registry%20is%20a,versions%20of%20a%20specific%20image        