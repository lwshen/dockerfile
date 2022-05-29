# dockerfile
A collection of dockerfile

## Portainer

Portainer is a management GUI for Kubernetes, Docker and Swarm. You can find the offical installation here: [https://docs.portainer.io/v/ce-2.9/start/install/server/docker/linux](https://docs.portainer.io/v/ce-2.9/start/install/server/docker/linux)

```
docker volume create portainer_data
```

```
docker run -d -p 8000:8000 -p 9443:9443 -p 9000:9000 --name portainer \
    --restart=always \
    -v /var/run/docker.sock:/var/run/docker.sock \
    -v portainer_data:/data \
    portainer/portainer-ce
```