# todo-app

### Start docker container

- Build docker image: `$ docker build -t todo-app .`; `-t` flag tags the image as `todo-app` and the `.` tells docker where to find the `Dockerfile`
- Run docker container: `$ docker run -dp 3000:3000 todo-app`; `-d` flag means detached mode and `-p` flag is used for exposing the port

### Remove docker container

- Get the ID of the container: `$ docker ps`
- Stop the container `$ docker stop <the-container-id>`
- Remove the container `$ docker rm <the-container-id>`

> Note: `$ docker rm -f <the-container-id>` stops the container and removes it at the same time

### `exec`ing into the container

- Interactive terminal: `$ docker exec -i <the-container-id> /bin/bash` (in case of node instances use `/bin/sh`)
- Execute one command and close the connection: `$ docker exec <the-container-id> cat /data.txt`; this will retrieve the contents of `data.txt` from inside the docker container

### Volumes

- Create named value: `$ docker volume create todo-db`
- Run docker container with named volume: `$ docker run -dp 3000:3000 -v todo-db:/etc/todos todo-app`; `-v` flag specifies the volume
- Get details about the named volume: `$ docker volume inspect todo-db`

### Inspiration

- [Docker - Get started guid](https://docs.docker.com/get-started/02_our_app/)
- [Sample application code](https://github.com/docker/getting-started/tree/master/app)
