# Docker Container

When you issue the command `run` in Docker specifying an image, Docker will download the image (if is not already in the system) and will create a process that live in a isolated world. This process will see only its image as filesystem.

You can try to run your hello-world image with this command:

`docker run hello-world`{{execute}}

Notice that the container started as configured in the image, printed something and exited.

You was able to run an simple Hello World application in a ubuntu "virtual" machine with a single command!
