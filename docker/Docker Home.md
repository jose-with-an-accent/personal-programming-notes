Docker is a tool that lets us launch and configure different software. 

We also use [[Docker Compose]] for some programs.

# Installing
On Ubuntu systems, `sudo apt install docker docker-compose` will do the trick. This will add docker, and a small program called docker-

# Benefits
Dependencies: A large company or project might be using different versions of node_modules or dependencies, and projects using different versions can be a bit wonky.

# How To Use
Docker is a system where every app is in a container. These containers are configured via an image, which can be built with a Dockerfile (a file literally named that way). There's a large number of programs like nginx which already have images, and can be run as simply as `docker docker run -t nginx ` -  but we can also create our own.

### Syntax
```
FROM alpine
ENTRYPOINT ["echo", "'hello world!'"]
```
Detailed documentation is here.

If we want to build our new image, we do `docker build . -t hello_world`. We also run `docker run -t hello_world ` to actually run it, and if things go according to plan, we have a simple hello world program.

Alpine Linux is a very simple version of Linux. 

[[Docker Compose]] is an important program to learn too. It's an alternative way to define a container, with its own images, ports, and other configs.