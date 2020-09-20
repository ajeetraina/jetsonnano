# Docker, K3s and Jetson Nano

<details><summary>
Running Minecraft on NVIDIA Jetson Nano using Docker with persistence
 </summary>
 <br>
 
 ```
 sudo docker run -d -p 25565:25565 \
                   -e EULA=true \
                   -e ONLINE_MODE=false \
                   -e DIFFICULTY=hard \
                   -e OPS=Gurvira3  \
                   -e MAX_PLAYERS=50 \
                   -e MOTD="welcome to GurviraWorld" \
                   -v /tmp/minecraft_data:/data \
                   --name mc 
                   itzg/minecraft-server
```
 
 </details>
