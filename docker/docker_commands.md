# Docker Command Reference

## Lifecycle & Execution

### Build Image
Build from a Dockerfile in the current directory.
`docker build -t <image_name> .`

### Run Container (Detached)
Run in background with port mapping.
`docker run -d -p <host_port>:<container_port> --name <container_name> <image_name>`

### Run Container (Interactive)
Run interactively and remove (`--rm`) upon exit.
`docker run --rm -it <image_name> /bin/bash`
*Note: Use `/bin/sh` for Alpine images.*

### Execute in Running Container
Enter a container that is already running.
`docker exec -it <container_id> /bin/bash`

### View Logs
Follow log output in real-time.
`docker logs -f <container_id>`

## Docker Hub & Registry

### Login
Authenticate with your Docker Hub account.
`docker login`

### Tag Image
Tag a local image for a repository/registry.
`docker tag <source_image> <username>/<repository>:<tag>`
*Example:* `docker tag gcc-cmake-lcov dmetal23/gcc-cmake-lcov:1.3`

### Push Image
Upload the tagged image to the registry.
`docker push <username>/<repository>:<tag>`
*Example:* `docker push dmetal23/gcc-cmake-lcov:1.3`

### Pull Image
Download an image from a registry.
`docker pull <username>/<repository>:<tag>`

## Inspection & Management

### List Running Containers
`docker ps`

### List All Containers
Includes stopped containers.
`docker ps -a`

### Stop Container
`docker stop <container_id>`

### Remove Container
`docker rm <container_id>`

## Cleanup

### Prune System
Remove unused images, containers, and networks.
`docker system prune`

### Deep Clean
Remove unused images, containers, networks, and volumes.
`docker system prune -a --volumes`