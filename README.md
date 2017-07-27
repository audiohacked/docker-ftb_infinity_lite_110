# Feed-The-Beast Infinity Lite 1.10 (Minecraft 1.10.2) in a Docker Container
To pull the image:
```
docker pull audiohacked/ftb_infinity_lite_110:stable
```

It's highly recommended run a named data volume:
```
docker volume create minecraft_ftb_infinity_lite_data
```

Then, run the server container:
```
docker run --detach --interactive --tty \
    --name ftb_infinity_lite \
    --volume minecraft_ftb_infinity_lite_data:/minecraft/world \
    --publish 25565:25565 \
    --env EULA=TRUE \
    audiohacked/ftb_infinity_lite_110:stable
```
