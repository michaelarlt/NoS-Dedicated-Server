# What?
This is a Dockerfile allowing you to run the No One Survived Dedicated 
Server inside of a Docker container, through Wine.

Docker Compose:
```
version: "3.2"

services:
  nos:
    image: f63nnkj4/nosdedicated:latest
    container_name: NoS
    restart: "unless-stopped"
    volumes:
      - /opt/nos-dedicated:/home/steam/nos-dedicated
    environment:
      - PUID=911
      - PGID=911
    ports:
      - 7777:7777/udp
      - 27015:27015/udp
```
