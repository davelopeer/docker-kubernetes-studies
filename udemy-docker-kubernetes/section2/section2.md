# Docker commands

## run
Runs a container based on a image. Commands can be passed to override image's default runner.
~~~
docker run [image] [commands]
~~~

-it: starts with command in terminal

## ps

List running containers.
~~~
docker ps 
~~~

--all: list all existendd containers.

docker run = docker create + docker star

## create

Generates an id of the container.
~~~
docker create [image]
~~~

## start
Starts created container. It can start stopped container as well.
~~~
docker start -a [id]
~~~

-a: print container output in terminal

## system prune
Remove stopped containers and builded cache.
~~~
docker system prune
~~~

## logs
Logs information that have been runned inside of a container. Do not reactivate the container.
~~~
docker logs [id]
~~~

## stop
Stop a running container, giving the container a little time to shut down.
~~~
docker stop [id]
~~~

## kill
Kill a running container immediately.
~~~
docker kill [id]
~~~

## exec
Allows to execute commands inside of a running container.
~~~
docker exec -it [id] [command]
~~~

-it: make process shows in terminal (-i + -t)

## shell
Opens a shell inside of the container.
~~~
docker exec -it [i] sh
~~~
