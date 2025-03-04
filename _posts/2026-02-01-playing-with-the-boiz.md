---
layout: post
title: "Playing With The Boiz"
---

This past summer I made a Minecraft server to play with some friends. One of them works at Microsoft and get a good amount of Azure credits per month. My initial hunch was to see if there was a pre-made Minecraft container image, or a pre-made instance image. There wasn't so I would have to build it out normally.

<steps on using azure interface>

Everythin went fine until starting the instance. There was an issue (with what again?). Once the instance was running I couldn't connect with my game client. Ports are on a allow-list i.e. only open what's allowed. First few start ups were manually, used system-md to get them going every restart.

Settings for making it more friendly.

skew: B2s
"No Rbac permissions:['Microsoft.Authorization/roleAssignments/write']"

25565

mc_java_server -dm java -Xmx2048M -Xms2048M -jar server.jar nogui

sudo su - minecraft -s /bin/bash

screen -S mc_java_server -dm java -Xmx2048M -Xms2048M -jar server.jar nogui
screen -ls

screen -r mc_java_server
screen -S mc_java_server -X quit

Ctrl + A, then D

https://www.digitalocean.com/community/tutorials/how-to-create-a-minecraft-server-on-ubuntu-22-04
https://www.cherryservers.com/blog/minecraft-server-ubuntu

ssh -i "C:\Users\hyx\Documents\minecraft-server.pem" minecraft-admin@<ip-address>

curl https://cdn.modrinth.com/data/O7RBXm3n/versions/g34oIg9D/InventoryProfilesNext-fabric-1.21.3-2.1.0.jar --output InventoryProfilesNext-fabric-1.21.3-2.1.0.jar

curl -OJ https://meta.fabricmc.net/v2/versions/loader/1.21.4/0.16.9/1.0.1/server/jar --output fabric-server.jar

cd /usr/local/games/minecraft_server/Java-modded
/usr/bin/java -Xmx2048M -Xms2048M -jar fabric-server.jar nogui

https://fabricmc.net/use/server/
https://modrinth.com/mod/quicksort/version/yocnZSr3
https://modrinth.com/mod/fabric-api/version/5tj7y3PJ
https://modrinth.com/plugin/worldedit/version/rIYOU6Ta

ops.json

[
    {
        "uuid": "??",
        "name": "??",
        "level": 4,
        "bypassesPlayerLimit": false
    }
]

systemctl status minecraft
sudo systemctl restart minecraft

auto updating server (hau doe)