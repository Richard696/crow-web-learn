## Dockerize

`docker build -t cpp-container . ` this command tell the docker to build an image with the name of cpp-container

To access the docker image via bash run:
`sudo docker -ti cpp-container bash` for Linux
`docker -ti cpp-container bash` for Windows

### Creating Volume

- `docker eun -v <host>:<container> -ti <image> bash`
- `-v` create a volume option
- `<host>` the directory on the host machine
- `<container>` the directory on the docker container
- `image` the name to run
