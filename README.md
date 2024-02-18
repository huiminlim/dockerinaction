# Docker in Action

## Getting Started

Install Docker Engine by following instructions [here](https://docs.docker.com/engine/install/ubuntu/).

Run the command to check that Docker Engine is working correctly.

```bash
sudo docker run hello-world
```

Follow the instructions [here](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-20-04) to run Docker without `sudo`.

## Common Commands

Running a container from image, detached to background. The container will be running automatically.

To run the programs interactive, use the `-it` flag.

To delete container after finishing run, use the `--rm` flag.

```bash
docker run --detach --name webcontainer nginx:latest
```

However, to create a container from an image but in stopped state, use the `create` command.

```bash
docker create --name webcontainer nginx:latest
docker start webcontainer
```

To check actively running containers, run the `ps` command.

```bash
docker ps
```

Containers can be restart and verified to be restarted correctly.

```bash
docker stop webcontainer # Stops the container
docker restart webcontainer
docker logs webcontainer
```

To run additional programs in a docker container, use the `exec` command.

```bash
docker exec webcontainer ls # Runs the ls command inside webcontainer
```

## Images

To pull an image only rather than spin containers up, use the `pull` command.

```bash
docker pull nginx:latest
docker pull quay.io/dockerinaction/ch3_hello_registry:latest # from alternate sources not from docker hub
```

To save the image as a tar file, use the `save` command. Then, load it using the `load` command.

```bash
docker save -o nginx.tar nginx:latest
docker load –i nginx.tar
```

A docker image can also be built using a dockerfile.

```bash
docker build -t test:latest ch3_dockerfile # ch3_dockerfile is a directory containing the Dockerfile
```

Images can be deleted using the `rmi` command.

```bash
docker rmi test:latest
```
