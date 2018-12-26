# 欢迎使用K8SEASY

------

K8SEASY 是一个一键安装K8S高可用集群的软件。它可以帮助企业一键搭建完私有云系统，帮助用户在多家云服务商里灵活切换，不再被任何服务商绑架！ 对! 所有的操作只需要一键！

有问题 请进QQ群 : 778526002

# 演示视频 请查看

单机一键安装

https://github.com/xiaojiaqi/k8seasy_release_page/blob/master/video/1.mp4?raw=true

三节点高可用一键安装

https://github.com/xiaojiaqi/k8seasy_release_page/blob/master/video/1.mp4?raw=true



## 优点:

* 无需翻墙下载任何镜像
* 多节点高可用生产集群也只需要一键部署， 支持keepalived,haproxy 组合
* 无需任何配置
* 完美支持Centos7.0 和Ubuntu 16.04/18.04

更新日志

2018.12.26 dashboard crack 成功，可以利用特殊porxy 通过https端口访问。granfan, nfs, prometheus 支持完成。paused 镜像更换成功。

2018.12.17 fix bug, 打开 controller manager health http port. 1.12.3 1.13.1 installer 002版本可用（感谢向小橙测试)

2018.12.15 kubernets 1.13.1 支持

2018.12.12 最新版 支持kubernetes 1.10.11  1.11.5 1.12.3 3个版本， 支持 Dashboard coredns了.

2018.12.8 安装完成后会自动生成dashboard.kueconfig 文件，利用它可以登录Dashboard.

2018.12.8 1.10.4 因为安全问题，放弃

2018.12.8 keepalived 支持, worker节点 bugfix, Role显示支持



## Download
 
### 免费版下载


#### 百度网盘
link: [Download](https://pan.baidu.com/s/1EKI6e_HiOkZMiYVKFo0MoQ)

#### 微云网盘
link: [Download](https://share.weiyun.com/50YeQ8z)

#### OneDriver
link: [Download](https://1drv.ms/f/s!AtfNCArUoXVMpjoRzUyc6PQXTtao)




# 5分钟安装一个高可用三中心节点的kubernetes系统



有任何安装问题 可以在这里给我留言， 或者加入qq 778526002 群提问 谢谢！









## 前言



>大家好，今天我向大家安利一款软件，这款软件是kubernetes的安装软件。 它的名字叫 k8seasy. 你可以从https://github.com/xiaojiaqi/k8seasy_release_page
下载这款软件。


>这款软件是一款kubernetes的安装软件， 也就是说用这款软件 你可以很容易地把一个kubernetes系统搭建起来，而且是3节点的高可用系统。完全可以使用在生产环境里。

>说到kubernetes,大家都很熟悉了，这是一款google出品的容器编排的软件。但是要安装kubernetes实在是太困难 太复杂了，虽然它自带了一款安装程序，但是在中国的互联网环境里，我只想说实在是根本不能用啊。官方的安装程序需要下载很多镜像，速度慢，经常失败,各种安装失败的问题在论坛里比比皆是，而且如果你想搭建高可用的生产环境，想利用二进制安装服务，目前还是做不到的。所以这款k8seasy软件就是来解决大家的痛点。

## 优点

>先说说这款软件的优点


* 第一 它完全不需要配置，一键完成，包括集群也是一键生成。

* 第二 不需要下载任何镜像，所有需要的模块组件都已经帮你准备好了，你只需要安装一下就可以了。

* 第三 完美支持了centos 7以后版本 ubutun16.04 18.04版本。覆盖了绝大多数的系统。

* 第四 它已经内置了最常用的镜像 比如dashboard 和cordns heapster, 内部的监控已经完成，直接可以使用。

* 第五 它安装所有的组件是以系统服务方式安装，以后启动停止都非常简单。 

* 最后 支持最新的kubernetes的版本 从1.10.11 1.11.5 到1.12.3，可以让大家第一时间
体验到最新的软件
* 最后提示一下k8seasy 对外部的要求 只有一点，它要求主机需要有一个IP 在192.168.1.0 - 192.168.10.0 这10个子网里，这是因为kubernetes的证书是预先生成的。所以证书只覆盖了这个区域。


首先我们打开下载中百度网盘链接，我们可以看到这3个版本，它们分别对应 kubernetes 的1.10.11 1.11.5 1.12.3 这3个版本。

github 网页
![image](https://raw.githubusercontent.com/xiaojiaqi/k8seasy_release_page/master/image/1.png)
  
网页下部的下载链接

![image](https://raw.githubusercontent.com/xiaojiaqi/k8seasy_release_page/master/image/2.png)  


百度网盘中可选择的版本
![image](https://raw.githubusercontent.com/xiaojiaqi/k8seasy_release_page/master/image/3.png)  


我们以1.11.5 为例 演示2个案例



## 案例一 在本机安装一个完整的kubernetes


在这一个案例里，我们将作下面的演示，在一台主机上使用k8seasy 安装一套kubernetes以及dashboard 然后登录dashboard, 最后再完美的删除掉它。



>首先我们下载k8seasy 的安装包，大概1.5G, 包括了所有的镜像。好了，启动以前查看一下 网络设备，只有 lo eth0 eth1,并没有kubernetes的组件存在。所以系统是干净的

![image](https://raw.githubusercontent.com/xiaojiaqi/k8seasy_release_page/master/image/5.png)  


同时我们可以看到这是一台centos 的主机，版本是 7.5。 好了 我们要开始安装了，安装的命令是什么呢？
一句话

**sudo ./installer --install**

就是这么简单，然后你可以看到，所有安装好的组件名称都会列在上面，然后一个功能完整的集群就安装好了，就这么简单。

好了完成了，大概1分钟。 一个完整的kubernetes 已经装好了。 我们运行 . /etc/profile 重新加载一下环境变量。
  

![image](https://raw.githubusercontent.com/xiaojiaqi/k8seasy_release_page/master/image/6.png)  
我们利用kubectl 命令查看一下，

**kubectl get nodes**

你可以看到一个master node 的集群已经建立好了, 主节点版本是1.11.5. 

![image](https://raw.githubusercontent.com/xiaojiaqi/k8seasy_release_page/master/image/7.png)  



现在我们需要查看一下dashboard,看看它是否运行正常。 首先 在k8seasy的目录里多了一个文件 dashboard.kubeconfig 文件，这个就是登录dashboard 的凭证。


![image](https://raw.githubusercontent.com/xiaojiaqi/k8seasy_release_page/master/image/8.png)  

将它下载下来,然后运行

**kubectl get services kubernetes-dashboard -n kube-system**

命令，我们可以从输出看到，dashboard 目前正在主机9638 端口侦听。


![image](https://raw.githubusercontent.com/xiaojiaqi/k8seasy_release_page/master/image/9.png)  


现在我们利用浏览器 访问 https://192.168.3.11:9638这个端口，因为证书的原因，我们需要先允许使用这个例外.

![image](https://raw.githubusercontent.com/xiaojiaqi/k8seasy_release_page/master/image/10.png)  


好了出现登录界面了。我们选择刚才的凭证。登录成功。

![image](https://raw.githubusercontent.com/xiaojiaqi/k8seasy_release_page/master/image/11.png) 


好了一切尽在掌控。 我们可以查看整个系统。这个系统可以用来学习，开发kubernetes, 一切都非常简便。

![image](https://raw.githubusercontent.com/xiaojiaqi/k8seasy_release_page/master/image/12.png) 


当我们不需要它的使用，请使用

**sudo ./installer --uninstall**

![image](https://raw.githubusercontent.com/xiaojiaqi/k8seasy_release_page/master/image/13.png) 

一切都被删除干净了，所有的服务都删除了，网络也恢复到一开始的状况，就这么简单





 

## 案例2 在多个节点上安装一个多节点高可用的系统




现在我们开始第二个案例 单机作为学习是够了，但是要作为生产环境还是不够的。现在我们演示三节点高可用系统的搭建，然后再演示如何不断加入新的节点到这个集群里
。

首先我准备了4台虚拟主机，它们的ip 分别是192.168.3.10,192.168.3.11,192.168.3.14,192.168.3.17.


![image](https://raw.githubusercontent.com/xiaojiaqi/k8seasy_release_page/master/image/14.png) 


* 在安装以前我们需要选择3台主机，作为系统的主节点，这里我选择192.168.3.10, 192.168.3.11, 192.168.3.14 这3台主机作为主节点。当有业务来的时候，这3台主机会互为备份为外部提供服务。
* 其次需要为3个主机准备一个虚拟IP, 虚拟IP是系统高可用的核心原理，它不属于任何一个节点，但是它可以漂浮在3台主机上，如果某台主机发生故障，它就会自动漂移到健康的节点上，这样就实现了高可用。这里我们选择192.168.3.250 做为虚拟ip.请注意 虚拟IP不能和现有的IP冲突。
* 为每台主机选择虚拟IP绑定的设备，这里都是eth1.

在运行安装以前，还需要在每台主机上运行 

**sudo ./installer --prepare**


这样就好了。 然后在3台主机上同时运行一样的命令。

**sudo ./installer --intall --masterip=192.168.3.11,192.168.3.10,192.168.3.14 --virtualip=192.168.3.250 --virtualipInterface=eth1**

其中masterip 就是指3台虚拟主机的地址，virtualip 就是浮动ip, 而virtualipInterface 就是主机使用的网络设备。

在同一个集群安装， masterip ,virtualip  这2个安装参数必须是一样的。

![image](https://raw.githubusercontent.com/xiaojiaqi/k8seasy_release_page/master/image/15.png)



稍加等待，一个系统就安装好了。


我们利用kubectl 命令查看一下节点情况，

**kubectl get nodes**


![image](https://raw.githubusercontent.com/xiaojiaqi/k8seasy_release_page/master/image/16.png) 


**kubectl get services kubernetes-dashboard -n kube-system**

命令，我们可以从输出看到，dashboard 目前正在主机9553端口侦听。

![image](https://raw.githubusercontent.com/xiaojiaqi/k8seasy_release_page/master/image/17.png)

 
现在我们利用浏览器 访问 https://192.168.3.10:9553  ，和刚才类似，使用dashboard.kubeconfig 凭证，登录进系统。


![image](https://raw.githubusercontent.com/xiaojiaqi/k8seasy_release_page/master/image/18.png) 

登录进去以后 ，你就能发现，3个节点已经被完全管理起来了。




可以这样认为，一个三节点的高可用kubernetes 已经搭建成功了。可是这并不够，我们还需要将其他的节点不断的加入这个集群，我们该怎么做呢？

很简单，在其他的主机节点上运行几乎完全一样的命令

**sudo ./installer --intall --masterip=192.168.3.11,192.168.3.10,192.168.3.14 --virtualip=192.168.3.250**

![image](https://raw.githubusercontent.com/xiaojiaqi/k8seasy_release_page/master/image/19.png) 

安装完成了，再次检查一下节点状态，新节点已经在集群里了。

![image](https://raw.githubusercontent.com/xiaojiaqi/k8seasy_release_page/master/image/20.png) 

再次进入监控，我们可以发现新节点也在集群里。所以任务完成

![image](https://raw.githubusercontent.com/xiaojiaqi/k8seasy_release_page/master/image/21.png) 

 
最后希望你提出宝贵意见，你可以在k8seasy@gmail.com  , https://github.com/xiaojiaqi/k8seasy_release_page,  以及QQ 群： 778526002 给出反馈。让我们把它变得更好。
