Docker Network is system that enables communication between docker containers, set ups connection between container and external network. If you use Docker Network, containers can communication in isolation from each other. Even you can also control your connection to external systems.
# Docker Network Structure
![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fdk8I8b%2FbtrWQ4y63lA%2FZbKBgSi9EYOu9jdXZkxfMK%2Fimg.png)               
Basically, Docker network is organized like a picture. `eth` mean network interface that host uses. And `docker0` and `my_bridge` is Docker's network interface. Finally, host network interface and Docker network interface connect through `veth`. The `veth` pair connects the docker's virtual network like a kind of cable.
# Docker Network Driver
Network Driver is configuration method that docker container communicate each other, help to connect external Network. Docker provides different types of network drivers to support different network environments, each of which is designed to fit specific network scenarios.
### Bridge
Containers use `bridge` networks by default, and containers on the same host can communicate with each other. To access a container from outside, you must connect a specific port on the host to a port on the container.
### Host
Create a container to use the host's network stack directly. In this case, the container does not have its own IP, but shares the host's IP address.
### Overlay
Connect containers across multiple hosts into a single virtual network, which is useful when used with orchestration tools such as dockerswarms and Kubernetes.
### macvlan
Assign a virtual network interface to the container that works similarly to the physical network interface, which results in the container having a real IP address on the same subnet as the host's network.
### none
Completely isolate the container from the network; the container does not have a network interface and cannot communicate with the outside world.

---
Reference link 🙂    
https://seosh817.tistory.com/373         
https://velog.io/@choidongkuen/서버-Docker-Network-에-대해             
https://devbksheen.tistory.com/entry/도커-네트워크docker-network-활용하기