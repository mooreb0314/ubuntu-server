# Minecraft PO3 Curseforge Pack
1. Create folder for persistant storage
```
mkdir ~/mc/mc_po3/data
```
2. Create 
```
docker run -d -v /home/bmoore/data_dirs/mc/mc_po3/data:/data -it -e EULA=TRUE -e TYPE=CURSEFORGE -e VERSION=1.12.2 -e MEMORY=16G -e CF_SERVER_MOD=https://minecraft.curseforge.com/projects/project-ozone-3-a-new-way-forward/files/2700952/download   -p 25565:25565 --name mc_po3 itzg/minecraft-server
```
3. 
2. Start Minecraft Server
```
docker start mc_po3
```
