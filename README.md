## An arm64 docker image for [scribble.rs](https://github.com/scribble-rs/scribble.rs) made by drifty

The official images hadn't been updated so I cloned the repo and built the image myself. Useful for anyone with an arm64 processor who wants to run scribble.rs 

Also available on the Docker Hub Registry - [```driftywinds/scribble.rs:latest```](https://hub.docker.com/repository/docker/driftywinds/scribble.rs)

How to use: - 

1. Follow instructions of the official repo from [here](https://github.com/scribble-rs/scribble.rs?tab=readme-ov-file#running-the-docker-container).
2. Remove or comment out the ```PORT:<port>``` line.
3. Replace the "image" part of the docker-compose.yml to ```driftywinds/scribble.rs:latest```.

<br>

You can check logs live with this command: - 
```
docker logs scribble-scribble.rs-1 -f
```
The container will be ready to use when the last line in the logs says ```Started, listening on: http://:8080```
