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
 
## Checking the logs

```
EST into 1.16.3
[init] Resolving type given VANILLA
[init] server.properties already created, skipping
[init] Setting/adding ops
[init] log4j2.xml already created, skipping
[init] Checking for JSON files.
[init] Setting initial memory to 1G and max to 1G
[init] Starting the Minecraft server...
[12:42:23] [main/INFO]: Environment: authHost='https://authserver.mojang.com', accountsHost='https://api.mojang.com', sessionHost='https://sessionserver.mojang.com', name='PROD'
```


 </details>

<details><summary>
Running Jtop to see what % of GPU is being consumed
 </summary>
 
## Installing Jtop 
 
sudo -H pip install -U jetson-stats

## Running the Jtop tool

sudo jtop

![My Image](https://github.com/ajeetraina/jetsonnano/blob/master/images/jtop.png)
</details>
