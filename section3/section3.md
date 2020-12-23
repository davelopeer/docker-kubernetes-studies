# Building Images

Dockerfile -> Docker Cliente -> Docker Server -> **Docker Image**

Creating a Dockerfile:

1. Specify a base image;
2. Run some commands to install additional programs;
3. Specify a command to run on container startup.


The Dockerfile is created using:

- And instruction telling Docker Server what to do (FROM, RUN, CMD..);
- Argument to the instruction.

## build
After creating a Dockerfile with specifications, build it with:
~~~
docker build .
~~~

Dockerserver follows the commands in Dockerfile and for each step it creates a new temporarily container with the configuration of the last step, removing the temporarily container after.

## cache

Docker build with cache to increase performance when the step have been already build. It caches the temporarily containers and re-use them if nothing was changed.

## tagging

Creates a name to use rather than the *docker image id*.
~~~
docker build -t [personal-docker-id]/[project-name]:[version] .
docker run [personal-docker-id]/[project-name]
~~~

*_Actually the tag is really just the [version]_

## commit
Creates an image based on a running container.
~~~
docker commit -c 'CMD ["redis-server"]' [container-id]
~~~

-c: specifying the *run command*