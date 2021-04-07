# Docker

* <code>docker run [image]</code>

    run image

    * **-d** Run container in the background 
    * 檢查本地是否存在指定的映像檔，不存在就從公有倉庫下載
    * 利用映像檔建立並啟動一個容器
    * 分配一個檔案系統，並在唯讀的映像檔層外面掛載一層可讀寫層
    * 從宿主主機設定的網路橋界面中橋接一個虛擬埠到容器中去
    * 從位址池中設定一個 ip 位址給容器
    * 執行使用者指定的應用程式
    * 執行完畢後容器被終止

* <code>docker stop [imageId]</code>

    stop image

* <code>docker image ls</code>

    list the image

* <code>docker ps --all</code>
* <code>docker ps -a</code>

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

* <code>docker start [container id]</code>

    Start an existed container.

* <code>docker exec -it [container id] /bin/bash</code>

    Enter to the container with an interactive and tty (Teletypewriter, 終端) mode 


---
## Dockerfile

* **FROM** specifies the Parent Image from which you are building


---

