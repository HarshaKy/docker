# docker
learning docker

ADD vs COPY

1. ADD supports URLs but this should not be used as there is no error handling. Instead, use curl.
2. ADD supports running from tar file.

RUN vs CMD vs ENTRYPOINT

1. RUN executes when building the image.
    a. RUN curl <<<URL>>>
    b. install packages etc..
2. CMD and ENTRYPOINT run when the container starts.
    a. ENTRYPOINT determines the main process to run. PID #1
    b. CMD is additional commadns to pass into ENTRYPOINT
    c. CMD can be overridden by passing in arguments to docker run command.

CLI options
1. -d to run in detached mode
2. -p to map ports
3. -P to choose a random port
4. -t to add a tag
5. -f to specify a Dockerfile / filename