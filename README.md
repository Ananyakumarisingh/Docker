# Docker

### Containers
Your basic isolated __Docker__ process. Containers are to virtual machines, as threads are to processes. Or you can think of them as larger-than-life `chroot` environments.

### Lifecycle

- __docker create__ - Creates a container but doesn't start it
- __docker rename__ - Allows the container to be renamed
- __docker run__ - Creates and start a container in one operation
- __docker rm__ - Deletes a container
- __docker update__ - Updates a container's resource limits
- __docker run --rm__ - Removes container when stopped
- __docker run -v $HOSTDIR-$DOCKERDIR__ - Maps a directory on the host to the Docker container; see also Volumes
- __docker run -v__ - Removes volumes associed with container
- __docker run --log-driver=syslog__ - Runs Docker with custom log driver

### Starting and Stopping

- __docker start__ - Starts a container, so it is running
- __docker stop__ - Stops a running container
- __docker restart__ - Stops and starts a container
- __docker pause__ - Pauses a running container, "freezing" it in place
- __docker unpause__ - Unpauses a running container
- __docker run wait__ - Blocks until running container stops
- __docker run kill__ - Sends a SIGKILL to a running container
- __docker run attach__ - Connects to a running container

If you want to integrate a container with a hpst process manager, start the daemon with `-r=false` then use docker `start -a`.

If you want to expose container ports through the host, see the exposing ports section.

### Information on Docker Containers, Processes and Performance

- __docker ps__ - Shows running containers
- __docker logs__ - Gets logs from container; you can use a custom log driver, but logs are only available for `json-file` and `journald` in 1.10
- __docker inspect__ - Looks at all info on a container (including IP address)
- __docker evens__ - Gets events from container
- __docker port__ - Shows public facing port to container
- __docker top__ - Shows running processes in container
- __docker stats__ - Shows containers' resource usage statistics
- __docker diff__ - Shows changed files in the container's filesystem
- __docker ps -a__ - Shows running and stopped containers
- __docker stats --all__ - Shows a running list of containers

### Import/Export (Backup/Restore)

- __docker cp__ - Copies files or folders between a container and the local filesystem
- __docker export__ - Turns container filesystem into tarball archive stream to STDOUT

### Executing Commands

- __docker exec__ - Executes a command in container

To enter a running container, attach a new shell process to a running container called foo, use: 
````bash
docker exec -it foo /bin/bash
````

### Images
Images are templates that Docker containers are based on. They are the foundation layer from which your container is launched, and your changed then become independent from it (as another layer)

### Lifecycle of Containers (Create, Run , Build, Commit)

- __docker images__ - Shows all images
- __docker import__ - Creates image from a tarball
- __docker build__ - Creates image from Dockerfile
- __docker commit__ - Creates an image from a container, pausing it temporarily if it is running 
- __docker rmi__ - Removes an image
- __docker load__ - Removes an image from a tar archive as STDIN, including images and tags (as of 0.7)
- __docker save__ - Saves an image to a tar archive stream to STDOUT with all parent layers, tags and versions (as of 0.7)

### Info

- __docker history__ - Shows history of image
- __docker tag__ - Tags an image to a name (local or registry)

### Cleaning up





