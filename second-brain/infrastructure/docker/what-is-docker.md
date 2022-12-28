> Docker is a tool that helps people run programs on their computers or servers. It's like a special box that you can put a program inside of, and then the program will always run the same way no matter where you put the box. This is helpful because sometimes programs need certain things to work, like other programs or special settings, and Docker makes sure that everything the program needs is always with it in the box. So you can just move the box around and the program will always work, without you having to worry about setting things up or making sure everything is in the right place.

---

[The Future of Linux Container](https://www.youtube.com/watch?v=wW9CAH9nSLs)
😭 this is awesome...

---

ref: [docker-guide-for-beginners](https://subicura.com/2017/01/19/docker-guide-for-beginners-1.html)

### What is docker?
- Docker is a software platform that allows you to run applications in containers.
- Containers are like virtual boxes that can hold different types of programs or execution environments, and they can be easily moved around to different systems.
- Using Docker, you can package up your programs and their dependencies into containers, which makes it easier to deploy and manage them on different servers or cloud platforms.

### Existing Virtual Machine vs. Docker
![[Pasted image 20221228182354.png]]

*How to fix this overhead? Isolate the process*
-> Technology that run process in isolated space

### Container and Image
#### *Image*
- a template that defines the content and structure of a container
- immutable, no state values
- Containers are created from images, which are templates that define the content and setup of a container. An image can be thought of as a blueprint for a container. When you start a container from an image, you create a container instance, which is a running instance of the container that you can interact with.
- ![[Pasted image 20221228182948.png]]

#### Docker Layer
: refers to a change made to an image
- An image is built up from a series of layers, each representing a change or instruction.
- Example
	- When you create an image, you might start with a base image that contains the operating system and some basic tools. Then, you might add a layer that installs a specific version of a programming language or a layer that adds your application code. Each of these changes represents a layer in the image.
- *Allow images to be built up incrementally, which makes them more efficient and easier to manage* You don't have to include the same content in multiple images.
#### Docker Image URL
: a reference to a Docker image that is stored on a registry
- registry: a repository for Docker images, and it can be either public or private.
- A Docker image URL consists of three main parts:
	- *The registry hostname*: This is the domain name or IP address of the registry where the image is stored. For example, `registry.hub.docker.com` is the hostname for Docker Hub, which is a public registry.
	- *The namespace*: This is the name of the organization or user that owns the image. For example, `myuser` is the namespace for an image owned by a user named `myuser`.
	- *The image name*: This is the name of the image itself. For example, `myapp` is the name of an image.
- an example of a Docker image URL: `registry.hub.docker.com/myuser/myapp`.
	- with version: `registry.hub.docker.com/myuser/myapp:1.0`
	- with commit id: `registry.hub.docker.com/myuser/myapp@sha256:abcdef01234567890`
