# Docker compose

The Docker Compose works as a way of connecting differente containers. It does this automatically when we define the *services* in the yaml file

## running

In order to run an image, we use:

```
docker-compose up
```

Flag:
- **--build**: re-build and image specified in the docker-compose file
- **-d**: launch in background


## stoping container

~~~
docker-compose down
~~~


## restart policies

- **"no"**: never attempt to restart this container
- **always**: always tries to restart this container
- **on-failure**: only restart if the container stops with an error code
- **unless-stopped**: always restart unless the developers forcibly stop it