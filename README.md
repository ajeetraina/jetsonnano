# Docker, K3s and Jetson Nano

<details><summary>
Running Minecraft on NVIDIA Jetson Nano using Docker with persistence
 </summary>
 <br>
 
 ## Pre-requisite:
 
 - NVIDIA Jetson Board flashed with SD card image(comes with Docker by default)
 
 
 ```
 sudo docker run -d -p 25565:25565 \
                   --gpus all \
                   -e EULA=true \
                   -e ONLINE_MODE=false \
                   -e DIFFICULTY=hard \
                   -e OPS=collabnix  \
                   -e MAX_PLAYERS=50 \
                   -e MOTD="welcome to Collabnix" \
                   -v /tmp/minecraft_data:/data \
                   --name mc 
                   itzg/minecraft-server
```
 
 </details>
