# docker
learning docker

ADD vs COPY

1. ADD supports URLs but this should not be used as there is no error handling. Instead, use curl.
2. ADD supports running from tar file.

RUN vs CMD vs ENTRYPOINT

1. RUN executes when building the image. <br>
    a. RUN curl <<<URL>>> <br>
    b. install packages etc.. <br>
2. CMD and ENTRYPOINT run when the container starts. <br>
    a. ENTRYPOINT determines the main process to run. PID #1<br>
    b. CMD is additional commadns to pass into ENTRYPOINT<br>
    c. CMD can be overridden by passing in arguments to docker run command.<br>

CLI options
1. -d to run in detached mode
2. -p to map ports
3. -P to choose a random port
4. -t to add a tag
5. -f to specify a Dockerfile / filename
6. --name to give a container a name
7. -v mount a volume to a container (folder from local machine)
8. -it interactive mode & tty

EXEC <br>
Used to run a new command in a running Docker container. Useful to interact with an already running container.
```
docker container exec -it 96e9721dfae6 /bin/bash
```