# How to Deploy PAPI-Jahat to Docker and Portainer
1. Copy `Dockerfile`, `docker-compose.yml`, `requirements.txt` and `src` folder to server, example: `/home/papi-jahat`
2. Open path using terminal
```
cd /home/papi-jahat
```
3. Create docker image and name it `snusnu/papi-jahat` and add version tag, example:
``` 
docker build -t snusnu/papi-jahat:0.2.0 .
```
5. Open Portainer and choose `Stack -> Add Stack`
6. Deploy the stack using existing `docker-compose.yml` or type it using `Web Editor`:
```
services:
  papi-jahat:
    build: .
    image: snusnu/papi-jahat:0.2.0
    container_name: papi-jahat
    ports:
      - 8888:8000
    restart: "unless-stopped"
    deploy:
      resources:
        limits:
          cpus: '0.5'
          memory: 128M
```