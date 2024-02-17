# Docker in Action

## Getting Started

Install Docker Engine by following instructions [here](https://docs.docker.com/engine/install/ubuntu/).

Run the command to check that Docker Engine is working correctly.

```bash
sudo docker run hello-world
```

Follow the instructions [here](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-20-04) to run Docker without `sudo`.

## Common Commands

Running a container from image, detached to background.

```bash
docker run --detach --name web nginx:latest
```
