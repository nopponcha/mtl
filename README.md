# Using Docker Buildx to Create Cross-Platform Docker Images for Seamless Compatibility

- Builder instance: For using docker buildx, there should be a builder instance up and running and for creating a builder instance fire docker buildx create --use.
$ docker buildx create --use --name buildx_instance buildx_instance

- docker buildx build command can be used for building images, the intresting option while building the image is --platform flag. In this command we are creating a image which is compatible with ARM as well as AMD processors.
$ docker buildx build --platform linux/amd64,linux/arm64,linux/arm/v7 -t noppon/hello_go_mtl:1.0.1 --push .

- Here is how it will be visible on dockerhub:
$ https://hub.docker.com/repository/docker/noppon/hello_go_mtl/tags?page=1&ordering=last_updated
