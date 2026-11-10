<div align="center">

```text
  _  _____                              _    ___ 
 | |/ ( _ ) ___  ___  __ _ ___ _   _   / \  |_ _|
 | ' // _ \/ __|/ _ \/ _` / __| | | | / _ \  | | 
 | . \ (_) \__ \  __/ (_| \__ \ |_| |/ ___ \ | | 
 |_|\_\___/|___/\___|\__,_|___/\__, /_/   \_\___|
                               |___/             
```

### Kubernetes 集群自动化安装工具

**纯二进制安装 · 纯离线部署 · 镜像资源内置 · 参数灵活可配**

从系统环境准备，到 Kubernetes 控制平面、网络与监控组件部署，  
通过清晰的命令完成集群安装，让部署流程更简单、更可控。

[核心特性](#核心特性) · [架构与要求](#架构与系统要求) · [部署 Demo](#部署-demo三节点高可用集群)

</div>

## 官方支持QQ：778526002


<div align="center">

 

<img src="https://raw.githubusercontent.com/xiaojiaqi/k8seasy_release_page/master/image/demo.gif" width="900" alt="k8seasyAI Demo">

</div>

## 🚀 核心功能

### 1. Kubernetes 版本支持

- 支持 Kubernetes **v1.35 及后续版本**。
- 支持从零开始自动化部署 Kubernetes 集群。
- 支持单节点和多节点集群部署。
- 支持 Master、Etcd 和 Worker 节点角色配置。
- 支持生产环境高可用（HA）集群架构。

### 2. 容器运行时支持

- 使用 **containerd** 作为容器运行时。
- **不支持 Docker** 作为 Kubernetes 容器运行时。
- 支持 containerd 自动化安装与配置。
- 支持容器运行时组件离线部署。

### 3. Kubernetes 网络插件

支持两种主流 Kubernetes 网络方案：

**Calico**
- 支持 Calico 自动化安装。
- 支持 VXLAN 网络模式。
- 支持 CrossSubnet 网络配置。

**Cilium**
- 支持 Cilium 自动化安装。
- 支持基于 eBPF 的高性能网络方案。
- 支持 Hubble Relay 和 Hubble UI。

### 4. 纯二进制安装

- 采用原生二进制安装方式。
- 无需 Docker 或其他容器化安装工具。
- Kubernetes 核心组件及相关工具采用二进制部署。
- 自动完成组件安装、配置和服务初始化。
- 减少外部依赖，简化部署流程。

### 5. 高可用集群部署（HA）

- 支持 1 节点和 3 节点 Master 架构。
- 支持 1 节点和 3 节点 Etcd 架构。
- 支持多节点 Worker 扩展。
- 支持独立 Etcd 集群部署。
- 支持生产环境 Kubernetes 高可用架构。

### 6. 纯离线安装

- 所有安装所需组件均可通过预先准备的软件包提供。
- 安装过程无需连接互联网。
- 无需在线下载 Kubernetes、Helm、网络插件及监控组件。
- 支持完整 Kubernetes 集群及附加组件离线部署。
- 适用于内网、隔离网络及无互联网访问的生产环境。

### 7. 完整监控系统支持（Monitor）

完整支持 Prometheus + Grafana 监控体系的二进制及离线部署。

- 支持 Prometheus 监控系统部署。
- 支持 Grafana 可视化监控平台部署。
- 支持 kube-prometheus-stack。
- 支持 Helm 二进制安装。
- 支持监控组件离线安装。
- 自动完成监控组件安装及 Kubernetes 集群接入。

## 📦 部署命令

| 命令 | 功能 |
|---|---|
| `key` | 生成集群配置及密钥文件 |
| `pre` | 系统环境检查及依赖准备 |
| `etcd` | Etcd 集群部署 |
| `api` | Kubernetes API Server 部署 |
| `node` | Kubernetes 节点部署 |
| `network` | Calico / Cilium 网络部署 |
| `monitor` | Prometheus / Grafana 监控部署 |

## 🎯 项目特点

- **Container Runtime:** containerd，不支持 Docker。
- **Kubernetes:** v1.35 及后续版本。
- **Networking:** Calico / Cilium。
- **Installation:** 原生二进制安装。
- **Deployment:** 完整离线部署，无需网络下载。
- **Architecture:** 支持生产级高可用集群。
- **Monitoring:** 完整支持 Prometheus + Grafana。

---

**从零开始，快速构建生产级 Kubernetes 集群。**





# k8seasyAI Release Notes

## Kubernetes Cluster Automated Installation Tool

k8seasyAI is an automated Kubernetes cluster deployment tool designed for production environments. It provides an end-to-end deployment solution, supporting both single-node installations and multi-node High Availability (HA) clusters.

This release focuses on Kubernetes v1.35+ compatibility, container runtime support, networking plugins, native binary installation, fully offline deployment, and integrated monitoring.

## 🚀 Key Features

### 1. Kubernetes Version Support

- Supports Kubernetes **v1.35 and later versions**.
- Automated Kubernetes cluster deployment from scratch.
- Supports single-node and multi-node deployments.
- Supports Master, Etcd, and Worker node roles.
- Supports production-ready High Availability (HA) architectures.

### 2. Container Runtime Support

- Uses **containerd** as the container runtime.
- **Docker is NOT supported** as a Kubernetes container runtime.
- Automated containerd installation and configuration.
- Supports offline deployment of container runtime components.

### 3. Kubernetes Networking Plugins

Supports two major Kubernetes networking solutions:

**Calico**
- Automated Calico installation.
- Supports VXLAN networking mode.
- Supports CrossSubnet configuration.

**Cilium**
- Automated Cilium installation.
- Supports high-performance eBPF-based networking.
- Supports Hubble Relay and Hubble UI.

### 4. Native Binary Installation

- Uses native binary-based installation.
- No Docker or other containerized installation tools required.
- Kubernetes core components and supporting tools are deployed using binaries.
- Automated component installation, configuration, and service initialization.
- Reduced external dependencies and simplified deployment workflows.

### 5. High Availability (HA) Deployment

- Supports 1-node and 3-node Master architectures.
- Supports 1-node and 3-node Etcd architectures.
- Supports multi-node Worker expansion.
- Supports dedicated Etcd cluster deployment.
- Designed for production-grade Kubernetes High Availability architectures.

### 6. Fully Offline Installation

- All required installation components are provided through pre-packaged software bundles.
- No internet connection required during installation.
- No online downloads of Kubernetes, Helm, networking plugins, or monitoring components.
- Supports complete offline Kubernetes cluster and add-on deployment.
- Ideal for private networks, isolated environments, and production infrastructure without internet access.

### 7. Integrated Monitoring System (Monitor)

Full support for binary-based and offline deployment of the Prometheus + Grafana monitoring stack.

- Prometheus monitoring system deployment.
- Grafana visualization platform deployment.
- Supports kube-prometheus-stack.
- Helm binary installation.
- Offline monitoring component installation.
- Automated monitoring deployment and Kubernetes cluster integration.

## 📦 Deployment Commands

| Command | Description |
|---|---|
| `key` | Generate cluster configuration and key files |
| `pre` | System environment checks and dependency preparation |
| `etcd` | Deploy the Etcd cluster |
| `api` | Deploy Kubernetes API Server |
| `node` | Deploy Kubernetes nodes |
| `network` | Deploy Calico / Cilium networking |
| `monitor` | Deploy Prometheus / Grafana monitoring |

## 🎯 Project Highlights

- **Container Runtime:** containerd (Docker is not supported).
- **Kubernetes:** v1.35 and later.
- **Networking:** Calico / Cilium.
- **Installation:** Native binary-based installation.
- **Deployment:** Fully offline installation, no network downloads required.
- **Architecture:** Production-grade High Availability support.
- **Monitoring:** Integrated Prometheus + Grafana monitoring.

---

**Build production-ready Kubernetes clusters from scratch — simply, reliably, and completely offline.**







---

## 项目简介

**k8seasyAI** 是一款面向 Kubernetes 二进制集群的自动化安装工具，提供从节点环境准备、etcd 安装、Kubernetes 控制平面部署，到 Worker 配置、网络插件和监控系统安装的完整流程。

它适用于单机测试、多节点集群、内网环境及需要离线部署的场景。集群节点角色和网络参数可以按实际环境规划配置。

## 核心特性

| 特性 | 说明 |
|---|---|
| **纯二进制安装** | 以 Kubernetes Server 二进制发行包为基础部署集群组件，安装流程清晰，便于管理和维护。 |
| **纯离线部署** | 面向无公网访问、内网和隔离环境设计，安装过程中无需在线下载 Kubernetes 镜像或安装配置。 |
| **镜像资源内置** | 发行资源包内置安装所需的镜像资源，减少部署时对外部镜像仓库的依赖。 |
| **支持较新 Kubernetes 版本** | 支持 Kubernetes **1.35.9 及后续版本**；具体版本应以所选二进制包及工具兼容性为准。 |
| **参数灵活可配** | 可配置 Master、etcd、Worker 节点 IP、Service 网段、Pod 网段、NTP 时间服务器及网络插件。 |
| **多种集群拓扑** | 支持单节点、多节点及多 Master / 多 etcd 部署，可按需组合节点角色。 |
| **网络与监控集成** | 支持安装 Calico 或 Cilium，并可部署 Prometheus 与 Grafana。 |

> **离线环境说明：** IPVS、Chrony 等系统基础软件及相关依赖仍需提前准备好软件包或可用的软件源。请在部署前核对目标操作系统、二进制包和组件版本的兼容性。

## 架构与系统要求

### 集群角色

```text
                   +--------------------------+
                   |      Kubernetes 集群     |
                   +-------------+------------+
                                 |
             +-------------------+-------------------+
             |                   |                   |
      +------+-------+    +------+-------+    +------+-------+
      |    Master    |    |     etcd      |    |    Worker    |
      |  控制平面    |    |  集群状态数据 |    |  运行工作负载 |
      +--------------+    +--------------+    +--------------+
```

| 角色 | 职责 |
|---|---|
| **Master** | 运行 Kubernetes 控制平面，负责集群管理与调度。 |
| **etcd** | 存储 Kubernetes 集群状态数据。 |
| **Worker** | 运行应用 Pod 和 Kubernetes 工作负载。 |

Master、etcd 和 Worker 可以部署在同一台主机，也可以分开部署。

- Master 支持 1 个或 3 个。
- etcd 支持 1 个或 3 个。
- Worker 节点可以按需扩展。
- 三节点 etcd 在正常组成集群后，通常可以容忍一个成员故障。
- Master 高可用还需要配置 API Server 的统一访问入口，例如负载均衡。

### 支持的操作系统

- Rocky Linux 9.0 及以上
- CentOS 7.9 及以上
- Ubuntu 18.04 及以上

### 发行包文件

```text
k8seasyAI/
├── K8seasyAI                  # 命令行安装工具
├── package.zip                # 安装资源包
├── package2.tar.gz            # 安装资源包
└── kubernetes.server.tar.gz   # Kubernetes Server 二进制发行包
```

运行 `key` 命令后，会在当前目录生成 `k8skey.key`，其中包含集群配置及安装所需的关键密钥信息。请将所需安装文件和密钥文件复制到每个目标节点，并妥善保管密钥。

Kubernetes Server 二进制包可从官方渠道获取：

- [Kubernetes 官方网站](https://kubernetes.io/)
- [Kubernetes GitHub Releases](https://github.com/kubernetes/kubernetes/releases)

## 命令速览

| 命令 | 功能 | 执行范围 |
|---|---|---|
| `key` | 生成集群配置文件和密钥文件 | 任意一台部署节点执行一次 |
| `pre` | 准备系统环境及依赖 | 所有节点 |
| `etcd` | 安装 etcd | 所有 etcd 节点 |
| `api` | 安装 Kubernetes 控制平面 | 所有 Master 节点 |
| `node` | 配置 Worker 节点 | 所有 Worker 节点 |
| `network` | 安装 Calico 或 Cilium | 一台 Master 执行一次 |
| `monitor` | 安装 Prometheus 和 Grafana | 一台 Master 执行一次 |

---

# 部署 Demo：三节点高可用集群

以下示例展示三台主机同时承担 Master、etcd 和 Worker 角色的安装流程。请将示例 IP 替换为实际节点 IP。

## 1. 节点规划

```text
192.168.1.1  Master + etcd + Worker
192.168.1.2  Master + etcd + Worker
192.168.1.3  Master + etcd + Worker
```

## 2. 生成集群配置

在 `192.168.1.1` 上执行：

```bash
sudo ./K8seasyAI key
```

根据交互提示配置：

- Master 节点数量及 IP
- etcd 节点数量及 IP
- Worker 节点 IP
- Service IP 网段
- Pod IP 网段
- NTP 时间服务器列表
- 网络组件：Calico 或 Cilium

执行完成后会生成 `k8skey.key`。将该文件和发行包所需文件复制到 `192.168.1.2` 与 `192.168.1.3`，并妥善保管密钥。

## 3. 所有节点准备环境

在三台节点上分别执行：

```bash
sudo ./K8seasyAI pre
```

**必须等待所有节点完成 `pre`，再进行后续安装。**

## 4. 安装 etcd 集群

在三台节点上分别执行：

```bash
sudo ./K8seasyAI etcd
```

安装完成后，可在具备相应证书的 etcd 节点检查健康状态：

```bash
sudo /opt/k8seasy/bin/etcdctl \
  --endpoints=https://127.0.0.1:2379 \
  --cacert=/etc/kubernetes/cert/ca.pem \
  --cert=/etc/kubernetes/cert/etcd.pem \
  --key=/etc/kubernetes/cert/etcd-key.pem \
  endpoint health
```

## 5. 安装 Kubernetes 控制平面

在三台 Master 节点上分别执行：

```bash
sudo ./K8seasyAI api
```

执行前请确认 etcd 集群已经正常运行。

## 6. 配置 Worker 节点

本案例三台主机都承担 Worker 角色，因此在三台节点上分别执行：

```bash
sudo ./K8seasyAI node
```

## 7. 安装网络与监控

任选一台 Master，分别执行一次：

```bash
sudo ./K8seasyAI network
sudo ./K8seasyAI monitor
```

`network` 会根据 `key` 阶段的选择安装 Calico 或 Cilium；`monitor` 用于安装 Prometheus 与 Grafana。

## 8. 检查集群状态

在 Master 节点上执行：

查看节点：

```bash
sudo /opt/k8seasy/bin/kubectl \
  --kubeconfig=/etc/kubernetes/admin.kubeconfig \
  get nodes -o wide
```

查看所有命名空间中的 Pod：

```bash
sudo /opt/k8seasy/bin/kubectl \
  --kubeconfig=/etc/kubernetes/admin.kubeconfig \
  get pods -A
```

检查 etcd：

```bash
sudo /opt/k8seasy/bin/etcdctl \
  --endpoints=https://127.0.0.1:2379 \
  --cacert=/etc/kubernetes/cert/ca.pem \
  --cert=/etc/kubernetes/cert/etcd.pem \
  --key=/etc/kubernetes/cert/etcd-key.pem \
  endpoint health
```

> 提示：`kubectl get cs` 在较新的 Kubernetes 版本中可能已弃用或无法提供预期信息。建议优先结合节点状态、Pod 状态及组件自身健康检查判断集群是否正常。

## 安装流程总览

```text
  key
   |
   v
  pre       所有节点
   |
   v
  etcd      所有 etcd 节点
   |
   v
  api       所有 Master 节点
   |
   v
  node      所有 Worker 节点
   |
   +-------> network   一台 Master 执行一次
   |
   +-------> monitor   一台 Master 执行一次
```

## 监控访问入口

| 组件 | 地址 | 默认凭据 |
|---|---|---|
| Grafana | `http://<节点IP>:30901` | 用户名：`admin`；密码：`k8seasy20111101` |
| Prometheus | `http://<节点IP>:30900` | 以实际部署配置为准 |

**安全建议：** 生产环境请及时修改 Grafana 默认密码，并通过防火墙或内网访问策略限制监控服务的访问范围。

---

## 其他部署拓扑

| 案例 | 节点规划 | 适用场景 |
|---|---|---|
| 单节点 | 1 台：Master + etcd + Worker | 测试、学习、功能验证 |
| 双节点 | 1 台：Master + etcd + Worker；1 台：Worker | 小型测试或轻量环境 |
| 三节点 | 3 台：Master + etcd + Worker | 小型高可用拓扑 |
| 五节点 | 3 台：Master + etcd；2 台：Worker | 控制平面与工作负载分离 |
| 十节点 | 3 台：Master；3 台：etcd；4 台：Worker | 角色分离的多节点部署 |

所有拓扑均应先在每台节点执行 `pre`。多节点部署时，必须在每个对应角色的节点上执行 `etcd`、`api` 或 `node`；`network` 和 `monitor` 各在一台 Master 上执行一次即可。

## 快速入口

```bash
sudo ./K8seasyAI          # 显示英文帮助
sudo ./K8seasyAI helpcn   # 显示中文帮助
sudo ./K8seasyAI demo     # 显示英文安装案例
sudo ./K8seasyAI democn   # 显示中文安装案例
```

---

## 版权与许可

版权所有 © k8seasyAI 作者。保留所有权利。

在保留完整版权声明的前提下，个人或组织可出于非商业目的免费使用、复制、修改及分发本作品。任何商业性使用，包括但不限于销售、出租、提供收费服务或集成进商业产品，均须事先取得作者书面授权。

本作品按“现状”提供，不附带任何明示或默示保证。作者不对因使用或无法使用本作品而产生的直接或间接损失承担责任。作者保留修改本声明的权利。
