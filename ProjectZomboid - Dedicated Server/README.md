# How to Install Zomboid Dedicated Server:
1. Install **Docker** and **Portainer** ([reference](https://youtu.be/4y0ksWu4wHw?si=2pmldLHE6-GZfwXB))
2. (***Optional***) Install **NGINX Proxy Manager** ([reference](https://youtu.be/fCJbw75DCZw?si=V-6yL4stDB4WisT-))
3. Create folder `ZomboidConfig` in your server, example: `/srv/dockerdata/ProjectZomboid/ZomboidConfig`
4. Create folder `ZomboidDedicatedServer` in your server, example: `/srv/dockerdata/ProjectZomboid/ZomboidDedicatedServer`
5. Copy `zomboid-dedicated-server.Dockerfile`  to your server, example: `/srv/dockerdata/ProjectZomboid/zomboid-dedicated-server.Dockerfile`
6. Add **Stack** in `Portainer` and use `docker-compose.yml` in **Stack Web Editor**
7. (***Optional***) Set `AntiCheatProtectionType21` to `false` in `ZomboidConfig/Server/Zomboid.ini`

