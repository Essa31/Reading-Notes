

# Docker

### Definition:

Docker is a set of platform as a service products that use OS-level virtualization to deliver software in packages called containers. ([source](https://en.wikipedia.org/wiki/Docker_(software)))

Meaning that Docker is a type of virtualization which allows multiple users/applications to run on the same machine.

### Install Docker (Windows):

In order to install Docker we need to [download the desktop app first](https://www.docker.com/get-started/) and create a free account.

After downloading make sure that Docker is done installing by writing:

    $ docker --version

Which would output the insalled Docker version.

### Some Docker commands:

| Command | Use |
|---------|-----|
| `$ docker info ` | Returns some important inforamtion about Docker, like the number of containers for example |
| `$ docker image ls` | Allows inspecting the current image |
| `$ docker container ls -la` | Allows inspecting the all containers within Docker |
| `$ docker image build .` | Builds a Docker image using a Docker file |

### Images and Containers:

**Images** are snapshots in a given time of what a project contains, while **Containers** are a running instances of images.




## Things I want to know more about

- None

## Resources

[sources1](https://wsvincent.com/beginners-guide-to-docker/)

[sources2](https://djangoforapis.com/library-website-and-api/)

