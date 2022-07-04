# 常用命令(docker +)

## 容器使用

### info

### run

#### -i

#### -t

#### -d

#### -P

#### --name

##### 容器命名

#### --rm：容器退出时自动清理容器内部的文件系统。

#### -h HOSTNAME 或者 --hostname=HOSTNAME： 设定容器的主机名，它会被写到容器内的 /etc/hostname 和 /etc/hosts。

#### --dns=IP_ADDRESS： 添加 DNS 服务器到容器的 /etc/resolv.conf 中，让容器用这个服务器来解析所有不在 /etc/hosts 中的主机名。

#### --dns-search=DOMAIN： 设定容器的搜索域，当设定搜索域为 .example.com 时，在搜索一个名为 host 的主机时，DNS 不仅搜索 host，还会搜索 host.example.com。

### ps

### logs

### start

### stop

### restart

### stats

### attach

#### 执行此命令进入容器， 退出时会导致容器退出。建议使用exec替换

### exec

### export

### import

### rm

#### 删除容器时，容器必须是停止状态

### docker container prune

#### 清理掉所有处于终止状态的容器

### port

### top

### inspect

## 镜像使用

### images

#### 列出本地主机上的镜像

### pull

#### 当我们在本地主机上使用一个不存在的镜像时 Docker 就会自动下载这个镜像的最新版本

#### 使用pull可以拉取指定版本

### search

#### 搜索镜像

### rmi

#### 删除镜像

### 创建镜像:build

#### 从已经创建的容器中更新镜像，并且提交这个镜像

##### 更新镜像之前，我们需要使用镜像来创建一个容器。

##### 在运行的容器内使用 apt-get update 命令进行更新。

-   apt-get是ubantu的命令
    

##### 在完成操作之后，输入 exit 命令来退出这个容器。

##### 我们可以通过命令 docker commit 来提交容器副本

#### 使用 Dockerfile 指令来创建一个新的镜像

##### 使用命令 docker build ， 从零开始来创建一个新的镜像

-   -t
    
-   Dockerfile 文件所在目录，可以指定Dockerfile 的绝对路径
    

##### Dockerfile文件

### tag

#### 镜像添加一个新的标签

## 容器连接

### 网络端口映射

#### 子主题

#### -P

### Docker 容器互联

### 了解即可。如果你有多个容器之间需要互相连接，推荐使用 Docker Compose

#### 容器命名

##### docker --name

#### 新建网络

##### docker network create -d bridge test-net

#### 运行一个容器并连接到新建的 test-net 网络:

##### docker run -itd --name test1 --network test-net ubuntu /bin/bash

### 配置 DNS

#### 宿主机的 /etc/docker/daemon.json

#### 配置完，需要重启 docker 才能生效

## Docker 仓库管理

### login

### logout

## DockerFile

## 详情参考：https://www.runoob.com/docker/docker-dockerfile.html

### FROM构建镜像基于哪个镜像

### MAINTAINER镜像维护者姓名或邮箱地址

### RUN构建镜像时运行的指令

### CMD运行容器时执行的shell环境

### VOLUME指定容器挂载点到宿主机自动生成的目录或其他容器

### USER为RUN、CMD、和 ENTRYPOINT 执行命令指定运行用户

### WORKDIR为 RUN、CMD、ENTRYPOINT、COPY 和 ADD 设置工作目录，就是切换目录

### HEALTHCHECH健康检查

### ARG构建时指定的一些参数

### EXPOSE声明容器的服务端口（仅仅是声明）

### ENV设置容器环境变量

### ADD拷贝文件或目录到容器中，如果是URL或压缩包便会自动下载或自动解压

### COPY拷贝文件或目录到容器中，跟ADD类似，但不具备自动下载或解压的功能

### ENTRYPOINT运行容器时执行的shell命令

## compose

## machine

### Docker Machine 是一种可以让您在虚拟主机上安装 Docker 的工具，并可以使用 docker-machine 命令来管理主机。Docker Machine 也可以集中管理所有的 docker 主机，比如快速的给 100 台服务器安装上 docker。

### Docker Machine 是一种可以让您在虚拟主机上安装 Docker 的工具，并可以使用 docker-machine 命令来管理主机。Docker Machine 也可以集中管理所有的 docker 主机，比如快速的给 100 台服务器安装上 docker。

## 子主题

### doker版的kP8s

# 常用配置

## /etc/docker/daemon.json

# 适用场景

## Web 应用的自动化打包和发布。自动化测试和持续集成、发布。在服务型环境中部署和调整数据库或其他的后台应用。从头编译或者扩展现有的 OpenShift 或 Cloud Foundry 平台来搭建自己的 PaaS 环境。

# 优势

## 1、快速，一致地交付您的应用程序

## 2、响应式部署和扩展

## 3、在同一硬件上运行更多工作负载

# 架构
## ![](https://docimg1.docs.qq.com/image/0junBlDWCD0ECxUVXBdguw.png?w=1390&h=682)