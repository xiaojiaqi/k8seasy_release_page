# 欢迎使用K8SEASY

------

K8SEASY 是一个一键安装K8S高可用集群的软件。它可以帮助企业一键搭建完私有云系统，帮助用户在多家云服务商里灵活切换，不再被任何服务商绑架！ 对! 所有的操作只需要一键！

   http://dl.k8seasy.com   下载最新版本

新计划：
   支持容器模式安装运行k8s

1. 支持Ubuntu
2.  支持 1.21 版本
3. 新增nginx-ingress, helm 组件， 支持自动发现。



有问题 请进QQ群 : 778526002

安装很简单， 一键安装，安装一个系统只需要 3 分钟, 安装好以后完整的监控也一并装好，可以直接使用。（不止支持单master 还支持3主机 高可用方案)

以下场景 都以master 主机节点为 192.168.2.50 为范例



**场景1： 只有一台机器192.168.2.50，想在上面安装一个k8s 集群，同时192.168.2.50 也作为工作节点进行服务。以后有其他机器可以加入这个集群 系统安装全套监控软件**

1. 创建集群， 在 192.168.2.50 上安装k8s 集群， 192.168.2.50 也作为工作节点 进行服务

```shell
#创建密钥 192.168.2.50 就是这个主机的ip， 运行后本地会生成一个k8skey.pem 文件，就是密钥文件
sudo ./installer --genkey -hostlist=192.168.2.50

#创建集群
sudo ./installer   -kubernetestarfile kubernetes-server-linux-amd64v1.18.2.tar.gz -masterip 192.168.2.50

```


![image](https://raw.githubusercontent.com/xiaojiaqi/k8seasy_release_page/master/image/fast3.gif)

2. 如果有新节点，将一个新节点加入这个集群，master 主机为 192.168.2.50 

2条命令即可

```shell
#将密钥复制到其他节点
cp ../k8skey.pem ./
#在新节点上运行以下命令，将机器加入集群
sudo ./installer   -kubernetestarfile kubernetes-server-linux-amd64v1.18.2.tar.gz -masterip 192.168.2.50

```
![image](https://raw.githubusercontent.com/xiaojiaqi/k8seasy_release_page/master/image/fast2.gif)



**场景2： 只有一台机器192.168.2.50，想在上面安装一个k8s 集群， 但是这个主机只做master 不会作为工作节点。以后其他机器加入这个集群， 同时系统也只安装基本dashboard 服务**

1. 创建集群， 在 192.168.2.50 上安装k8s 集群， 192.168.2.50 并不作为工作节点

```shell
#创建密钥 192.168.2.50 就是这个主机的ip，运行后本地会生成一个k8skey.pem 文件，就是密钥文件
sudo ./installer --genkey -hostlist=192.168.2.50

#创建集群 同时不作为工作节点
sudo ./installer   -kubernetestarfile kubernetes-server-linux-amd64v1.18.2.tar.gz -masterip 192.168.2.50  --skipDocker=1

```

2. 将一个新节点加入这个集群，master 主机为 192.168.2.50 

2条命令即可

```shell
#将密钥复制到其他节点
cp ../k8skey.pem ./
#在新节点上运行以下命令，将机器加入集群
sudo ./installer   -kubernetestarfile kubernetes-server-linux-amd64v1.18.2.tar.gz -masterip 192.168.2.50  --dashboardOnly=1
（只有第一台工作节点 需要加入时加上 --dashboardOnly=1 参数， 后面的节点 可以使用  sudo ./installer   -kubernetestarfile kubernetes-server-linux-amd64v1.18.2.tar.gz -masterip 192.168.2.50 ）

```



 **场景3：  有3台机器192.168.2.50, 192.168.2.51,192.168.2.52，想在上面安装一个k8s 集群， 作为3节点高可用集群，这3个主机只做master 不会作为工作节点。以后其他机器加入这个集群， 同时系统也只安装基本dashboard 服务**

1. 创建集群， 在 192.168.2.50, 192.168.2.51,192.168.2.52 上安装k8s 集群， 这3个节点 并不作为工作节点

```shell
#创建密钥 192.168.2.50 就是这个主机的ip，运行后本地会生成一个k8skey.pem 文件，就是密钥文件
sudo ./installer --genkey -hostlist=192.168.2.50
#在3个节点上分别运行， 进行准备工作。 
sudo ./installer -prepare
#同时在3个节点上运行 安装命令， 注意是同时。必须同时运行
sudo ./installer   -kubernetestarfile kubernetes-server-linux-amd64v1.18.2.tar.gz -masterip 192.168.2.50,192.168.2.51,192.168.2.52  --skipDocker=1

```

1. 将一个新节点加入这个集群，master 主机为 192.168.2.50, 192.168.2.51,192.168.2.52 

2条命令即可

```shell
#将密钥复制到其他节点
cp ../k8skey.pem ./
#将机器加入集群
sudo ./installer   -kubernetestarfile kubernetes-server-linux-amd64v1.18.2.tar.gz -masterip 192.168.2.50,192.168.2.51,192.168.2.52  --dashboardOnly=1
（只有第一台工作节点 需要加入时加上 --dashboardOnly=1 参数， 后面的节点 可以使用  sudo ./installer   -kubernetestarfile kubernetes-server-linux-amd64v1.18.2.tar.gz -masterip 192.168.2.50,192.168.2.51,192.168.2.52 ）

```



一切就是这么简单！！


安装视频可以看这个

[优酷](https://v.youku.com/v_show/id_XNDU1MDQxNjExMg==.html)


或者
[爱奇艺](https://www.iqiyi.com/v_19rvrdfn18.html)


在 Azure 上安装成功！

## Download

### 免费版下载


#### 官网下载
link: [Download](http://dl.k8seasy.com/)

## 优点:

* 无需翻墙下载任何镜像
* 多节点高可用生产集群也只需要一键部署， 支持keepalived,haproxy 组合
* 无需任何配置
* 完美支持Centos7.0 和Ubuntu 16.04/18.04

最后希望你提出宝贵意见，你可以在k8seasy@gmail.com  , https://github.com/xiaojiaqi/k8seasy_release_page,  以及QQ 群： 778526002 给出反馈。让我们把它变得更好。
