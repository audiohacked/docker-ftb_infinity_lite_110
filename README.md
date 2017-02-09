# Feed-The-Beast Infinity Lite 1.10 (Minecraft 1.10.2) in a Docker Container
To pull the image:
```
docker pull audiohacked/ftb_infinity_lite_110:stable
```

It's highly recommended run a data container:
```
docker run --name ftb_infinity_lite_datastore audiohacked/ftb_infinity_lite_110:stable true
```

Then, run the server container:
```
docker run --detach --interactive --tty \
    --name ftb_infinity_lite \
    --volumes-from ftb_infinity_lite_datastore \
    -p 25565:25565 \
    -e EULA=TRUE \
    audiohacked/ftb_infinity_lite_110:stable
```
