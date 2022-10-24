It is assumed that you are familiar with basic `docker` commands. Docker should be properly installed and running in your system. 

## Install


Pull the [official docker image](https://hub.docker.com/r/aahnik/tgcf) from DockerHub.

```shell
docker pull aahnik/tgcf
```

> **Tip**: Use `aahnik/tgcf:minimal` for a smaller image size. (beta)

## Configure

- Set the password for web interface. `echo "PASSWORD=hocus pocus qwerty utopia" >> .env`

## Run

```shell
docker run -d -p 8501:8501 --env-file .env aahnik/tgcf
```

Note:
- the `-d` flag tells the docker command to run the container in detached mode.
- the `--env-file` option passes the file `.env` for its variables to be used inside the container.


## Check

To see if your container is running,

```shell
$ docker ps
CONTAINER ID   IMAGE         COMMAND                 CREATED          STATUS          PORTS                    NAMES
d12ef4fe2b6c   aahnik/tgcf   "/bin/sh -c tgcf-web"   32 seconds ago   Up 32 seconds   0.0.0.0:8501->8501/tcp   beautiful_mclean

```

The container id and name will be different in your machine.

**Visit [`localhost:8501`](http://localhost:8501/) to access the web interface for tgcf.**

To see the logs produced by the container,

```shell
$ docker logs zen_gates
```

Replace `zen_gates` with the name of the container in your machine.



