# minecraft-server

## Les références

 * https://hub.docker.com/r/itzg/minecraft-server/
 * https://github.com/itzg/docker-minecraft-server/tree/master/examples

## View logs

```
docker logs -f mc
```

## Pour accéder à la console du server

```
docker exec -i mc rcon-cli
```

## Healthcheck

```
docker container inspect -f "{{.State.Health.Status}}" mc
docker exec mc mcstatus localhost status
```


