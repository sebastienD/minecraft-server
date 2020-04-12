# minecraft-server

## Les références

 * https://hub.docker.com/r/itzg/minecraft-server/
 * https://github.com/itzg/docker-minecraft-server/tree/master/examples

 * https://cloud.google.com/solutions/gaming/minecraft-server
 * https://cloud.google.com/blog/products/gcp/brick-by-brick-learn-gcp-by-setting-up-a-minecraft-server

## Pour regarder les logs

```
docker logs -f minecraft
docker logs -f rcon
```

## Pour accéder à la console du server

```
docker exec -i minecraft rcon-cli
```

## Healthcheck

```
docker container inspect -f "{{.State.Health.Status}}" minecraft
docker exec minecraft mcstatus localhost
```

## Install forge

```
wget https://files.minecraftforge.net/maven/net/minecraftforge/forge/1.15.2-31.1.0/forge-1.15.2-31.1.0-installer.jar
```

Lancer l'installation dans le répertoire où se trouve le server.jar.
```
java -jar forge-1.15.2-31.1.0-installer.jar --installServer
```

## Lancer forge

```
java -Xmx3G -Xms1G -jar -d64 forge-1.15.2-31.1.0.jar nogui
```