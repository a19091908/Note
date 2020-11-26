# Docker

* <code>docker run [image]</code>

    run image

* <code>docker image ls</code>

    list the image

* <code>docker ps --all</code>

    List the container (spawned by the image) which exits after displaying its message. 

    If it is still running, you do not need the --all option.

* <code>docker build --tag bulletinboard:1.0 .</code>

    * build an image from a Dockerfile, and the tag of the image is bulletinboard:1.0
    * **-t** or **--tag** tags the image into multiple repositories
    * **-f** or **--file** specifies the path of Dockerfile


* <code>docker run --publish 8000:8080 --detach --name bb bulletinboard:1.0</code>

    * **--publish** asks Docker to forward traffic incoming on the host’s port 8000 to the container’s port 8080. Containers have their own private set of ports, so if you want to reach one from the network, you have to forward traffic to it in this way. Otherwise, firewall rules will prevent all network traffic from reaching your container, as a default security posture.
    * **--detach** asks Docker to run this container in the background.
    * **--name** specifies a name with which you can refer to your container in subsequent commands, in this case bb.


* <code>docker rm --force bb</code>

    The **--force** option stops a running container, so it can be removed. If you stop the container running with <code>docker stop bb</code> first, then you do not need to use **--force** to remove it.


* <code>docker ps --all</code>


* <code>docker ps --all</code>
