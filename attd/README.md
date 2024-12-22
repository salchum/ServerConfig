# How to Deploy attd to Docker and Portainer
1. Copy `Dockerfile`, `docker-compose.yml`, `requirements.txt` and `src` folder to server, example: `/home/attd`
2. Open path using terminal
```
cd /home/attd
```
3. Create docker image and name it `snusnu/attd-gen2` and add version tag, example:
``` 
docker build -t snusnu/attd-gen2:3.1.1 .
```
5. Open Portainer and choose `Stack -> Add Stack`
6. Deploy the stack using existing `docker-compose.yml` or type it using `Web Editor`:
```
services:
  attd-gen2:
    build: .
    image: snusnu/attd-gen2:3.1.1
    container_name: attd-gen2
    restart: "unless-stopped"
    deploy:
      resources:
        limits:
          cpus: '0.5'
          memory: 128M
```