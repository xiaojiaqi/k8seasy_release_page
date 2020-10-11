# 欢迎使用K8SEASY

------

K8SEASY 是一个一键安装K8S高可用集群的软件。它可以帮助企业一键搭建完私有云系统，帮助用户在多家云服务商里灵活切换，不再被任何服务商绑架！ 对! 所有的操作只需要一键！

新版本发布，支持 1.19.x  新增nginx-ingress, helm 组件， 支持自动发现。

有问题 请进QQ群 : 778526002

kubernetes v1.18.2 版本 已经支持, 所有监控为最新版本.

安装很简单， 一键安装，安装一个系统只需要 3 分钟, 安装好以后完整的监控也一并装好，可以直接使用。（不止支持单master 还支持3master 高可用方案)

2条命令即可

```shell
#创建密钥
sudo ./installer --genkey -hostlist=192.168.2.50

#创建集群
sudo ./installer   -kubernetestarfile kubernetes-server-linux-amd64v1.18.2.tar.gz -masterip 192.168.2.50

```


![image](https://raw.githubusercontent.com/xiaojiaqi/k8seasy_release_page/master/image/fast3.gif)


将一个新节点加入这个集群也只需要一个命令 

1条命令即可

```shell
 
#将密钥复制到本地
cp ../k8skey.pem ./
#将机器加入集群
sudo ./installer   -kubernetestarfile kubernetes-server-linux-amd64v1.18.2.tar.gz -masterip 192.168.2.50

```
![image](https://raw.githubusercontent.com/xiaojiaqi/k8seasy_release_page/master/image/fast2.gif)

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
