Docker Network is system that enables communication between docker containers, set ups connection between container and external network. If you use Docker Network, containers can communication in isolation from each other. Even you can also control your connection to external systems.
# Docker Network Structure
![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fdk8I8b%2FbtrWQ4y63lA%2FZbKBgSi9EYOu9jdXZkxfMK%2Fimg.png)               
Basically, Docker network is organized like a picture. `eth` mean network interface that host uses. And `docker0` and `my_bridge` is Docker's network interface. Finally, host network interface and Docker network interface connect through `veth`.

---
Reference link 🙂    
https://seosh817.tistory.com/373         
https://velog.io/@choidongkuen/서버-Docker-Network-에-대해             
https://devbksheen.tistory.com/entry/도커-네트워크docker-network-활용하기