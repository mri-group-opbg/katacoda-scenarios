# Docker Container

When you issue the command `run` in Docker specifying an image, Docker will download the image (if is not already in the system) and will create a process that live in a isolated world. This process will see only its image as filesystem.

You can try to run a complete ubuntu system with this command:

```
docker run -it ubuntu:18.04 bash
```

> The command run the container named ubuntu and open a bash shell in it. The parameter `-it` is needed to have an interactive shell into the container.

After the command you will see a prompt like `root@<hash>`: the has is the hostname of the machine you created!

Play with your container with command like:

```
apt-get update
```

```
apt-get install -y python
```

Enter in python with

```
python
```

Exit from python command line:

```
quit()
```

Exit from container

```
exit
```

Now that you are in the system, notice that python is not installed: all operations were performed inside the container.


