# Making a real project

**Steps**:

1. Create a node.js web app
2. Create a dockerfile
3. Build an image from dockerfile
4. Run image as container
5. Connect to web ap from a browser

## copy

Docker image command that copies files from the local machine to the temporarily container been processed in docker build
~~~
COPY [path-in-local-machine] [path-in-the container]
~~~

## port mapping

In order to access an specific port inside a container, we must run docker conecting the container port with your local port
~~~
docker run -p [localhost-port]:[container-port] [container-id]
~~~

## minimizing cache busting and rebuilds

- When we make a change in the code, our project rebuilds the steps after the files modificated, slowing the whole process of rebuild. 
- We can make changes in the Dockerfile to re-arrange the build for caching the process step-by-step.