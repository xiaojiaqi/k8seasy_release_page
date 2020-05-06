# 欢迎使用K8SEASY

------

K8SEASY 是一个一键安装K8S高可用集群的软件。它可以帮助企业一键搭建完私有云系统，帮助用户在多家云服务商里灵活切换，不再被任何服务商绑架！ 对! 所有的操作只需要一键！

原有版本将做大的更新，新版本以1.18为支持目标。主要升级监控相关组件

有问题 请进QQ群 : 778526002

kubernetes v1.18.2 版本 已经支持, 所有监控为最新版本.

安装视频可以看这个

[优酷](https://v.youku.com/v_show/id_XNDU1MDQxNjExMg==.html)


或者
[爱奇艺](https://www.iqiyi.com/v_19rvrdfn18.html)


在 Azure 上安装成功！

 <img src="https://raw.githubusercontent.com/xiaojiaqi/k8seasy_release_page/master/image/azure_1.png" width="800" height="600"> 

## Download
 
### 免费版下载


#### 百度网盘
link: [Download](http://dl.k8seasy.com/)

#### Google drive
link: [Download](https://drive.google.com/drive/folders/1JtLwZANly7dxr-xO4vaZ_bP7x8TGL8xy?usp=sharing)


安装视频

![安装视频](https://raw.githubusercontent.com/xiaojiaqi/k8seasy_release_page/master/image/installer.gif)

使用视频

![使用视频](https://github.com/xiaojiaqi/k8seasy_release_page/blob/master/image/webgui.gif)




# 演示视频 请查看

单机一键安装

https://github.com/xiaojiaqi/k8seasy_release_page/blob/master/video/1.mp4?raw=true

三节点高可用一键安装

https://github.com/xiaojiaqi/k8seasy_release_page/blob/master/video/2.mp4?raw=true



## 优点:

* 无需翻墙下载任何镜像
* 多节点高可用生产集群也只需要一键部署， 支持keepalived,haproxy 组合
* 无需任何配置
* 完美支持Centos7.0 和Ubuntu 16.04/18.04

更新日志

2019.12.04 最新版本，支持根据网络生成密钥，不再使用内置密钥。支持云环境高可用安装。
2019.7.20  最新版本，支持1.15.0 可以选择不同版本，支持离线安装。

2019.4.2 经过长长的休息，我准备release下一个版本。 这个版本会有一些不一样。安装包会自带有2个包，一个是kubernetes 本身的包，比如14.0 版本，你可以下载官方的包，来决定需要安装好的kubernetes版本。另一个包是和kubernetes相关的包 比如docker，docker镜像这样的包。这样的话，以后整个包的升级会非常轻量化。 升级只需要升级可执行文件，其他的包可以自行升级。不需要统一下载。

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

* 最后 支持最新的kubernetess所有版本 可以让大家第一时间体验到最新的软件
 
 
最后希望你提出宝贵意见，你可以在k8seasy@gmail.com  , https://github.com/xiaojiaqi/k8seasy_release_page,  以及QQ 群： 778526002 给出反馈。让我们把它变得更好。
