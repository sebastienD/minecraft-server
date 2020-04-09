# minecraft-server

## Les références

 * https://hub.docker.com/r/itzg/minecraft-server/
 * https://github.com/itzg/docker-minecraft-server/tree/master/examples

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


