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

To run the programs interactive, use the `-i` flag.

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
