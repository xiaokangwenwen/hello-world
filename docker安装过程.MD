编写：张晓慷  
时间：2019/03/19  
主题：docker安装过程记录  

# 1、简介
Docker是一个开放源代码软件项目，让应用程序部署在软件货柜下的工作可以自动化进行，借此在Linux操作系统上，提供一个额外的软件抽象层，以及操作系统层虚拟化的自动管理机制[1]。
Docker利用Linux核心中的资源分离机制，例如cgroups，以及Linux核心名字空间（namespaces），来创建独立的容器（containers）。这可以在单一Linux实体下运作，避免引导一个虚拟机造成的额外负担[2]。Linux核心对名字空间的支持完全隔离了工作环境中应用程序的视野，包括进程树、网络、用户ID与挂载文件系统，而核心的cgroup提供资源隔离，包括CPU、存储器、block I/O与网络。从0.9版本起，Dockers在使用抽象虚拟是经由libvirt的LXC与systemd - nspawn提供界面的基础上，开始包括libcontainer库做为以自己的方式开始直接使用由Linux核心提供的虚拟化的设施，
依据行业分析公司“451研究”：“Dockers是有能力打包应用程序及其虚拟容器，可以在任何Linux服务器上运行的依赖性工具，这有助于实现灵活性和便携性，应用程序在任何地方都可以运行，无论是公有云、私有云、单机等。

简单理解成，一个高效的虚拟机。基于Go语言开发；区别于Scratchbox（是一个帮助嵌入式Linux跨平台编译工具的集合，其目的主要是使得嵌入式Linux应用程序开发更加容易，他也提供了完整的集成工具链以用来跨平台编译集成出一个Linux发行版）

# 2、安装过程
## 安装环境
	ubuntu16.04 x64 
## 安装过程
+ sudo apt-get install docker.io (名字不是直接docker 的原因是linux已经有个软件叫docker了，类似于界面上的开始的东东）
+ 可以通过友善之臂提供安装镜像 https://github.com/friendlyarm/friendlyelec-ubuntu16-docker  
+ docker镜像的存储目录是/var/lib/docker
# 3 Docker扩展阅读
+ [docker教程RUNOOB](http://www.runoob.com/docker/docker-tutorial.html)
+ [Docker官方网站](https://www.docker.com/)
+ [Dockerfile 参考](https://docs.docker.com/engine/reference/builder/)
# 4 Docker常用指令
+ docker ps //查看当前的正在运行的容器
+ docker run //运行一个容器
+ docker build //创建本地镜像，根据Dockerfile创建本地的镜像文件
+ 更多详细指令参照 RUNOOB 教程
+ end 