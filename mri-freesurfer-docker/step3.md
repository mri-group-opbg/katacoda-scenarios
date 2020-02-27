# An interactive example

Let'd try to run a complete ubuntu system with the command:

`docker run -it ubuntu:18.04 bash`{{execute}}

> The command run the container named ubuntu and open a bash shell in it. The parameter `-it` is needed to have an interactive shell into the container.

After the command you will see a prompt like `root@<hash>`: the has is the hostname of the machine you created!

Play with your container with commands:

`apt-get update && apt-get install -y python`{{execute}}

Open python shell and play in python:

`python`{{execute}}

Exit from python command line:

`quit()`{{execute}}

Exit from container

`exit`{{execute}}

Simple eh!