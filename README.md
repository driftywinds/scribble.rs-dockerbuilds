## An arm64 docker image for [scribble.rs](https://github.com/scribble-rs/scribble.rs) made by drifty

The official images hadn't been updated so I cloned the repo and built the image myself. Useful for anyone with an arm64 processor who wants to run scribble.rs 

Also available on the Docker Hub Registry - [```driftywinds/scribble.rs:latest```](https://hub.docker.com/repository/docker/driftywinds/scribble.rs)

How to use: - 

1. Make a file called ```compose.yml```
2. Paste this into it: - 
```
version: "2.4"
services:
    scribble.rs:
        pull_policy: always
#        environment:
#            - PORT=3014
        ports:
            - 3014:8080
        image: ghcr.io/driftywinds/scribble.rs:latest
```
3. Type ```docker compose up -d```

<br>

You can check logs live with this command: - 
```
docker logs scribble-scribble.rs-1 -f
```
The container will be ready to use when the last line in the logs says ```Started, listening on: http://:8080```
