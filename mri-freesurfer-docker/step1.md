# Docker Image

A Docker image is a complete filesystem with operating system files, libraries, application and its dependencies.

Docker images are saved on a Docker Registry.

You can look for Docker images with the command `search`.

Try to run

```
docker search hello-world
```

You will see all the images that people created with the world `hello-world` in the name.

Docker images have as name `<repository>/<image_name>`

You can download ad image with the command `pull`:

```
docker pull hello-world
```
