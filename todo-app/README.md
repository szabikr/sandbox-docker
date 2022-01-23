# todo-app

### Start docker container

- Build docker image: `$ docker build -t todo-app .`; `-t` flag tags the image as `todo-app` and the `.` tells docker where to find the `Dockerfile`
- Run docker container: `$ docker run -dp 3000:3000 todo-app`; `-d` flag means detached mode and `-p` flag is used for exposing the port

### Inspiration

- [Docker - Get started guid](https://docs.docker.com/get-started/02_our_app/)
- [Sample application code](https://github.com/docker/getting-started/tree/master/app)
