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

### Access the Web in the container from the machine

`sudo docker run -v /home/yeeheng/learn/cpp/crow-web-learn:/usr/src/crow-web-learn -p 8080:8080 -e PORT=8080 cpp-container:latest /usr/src/crow-web-learn/crow_prj/build/crow_prj`
