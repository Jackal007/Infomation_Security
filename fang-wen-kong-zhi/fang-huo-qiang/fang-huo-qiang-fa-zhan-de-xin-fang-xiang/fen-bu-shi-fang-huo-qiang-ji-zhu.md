# 分布式防火墙技术

* ##### 网络防火墙\(Network Firewall\)

  纯软件实现或辅以硬件支持。用于内部网与外部网之间以及内部网各子网之间的防护。  
  与传统的边界防火墙相比，多了一种用于对内部子网之间的安全防护层，这样整个网络的安全防护体系就显得更加全面，更加可靠。不过在功能上与传统的边界防火墙相似。

* ##### 主机防火墙\(Host Firewall\)

  纯软件实现或辅以硬件支持。用于对网络中的服务器和桌面机进行防护。  
  相当于对传统边界式防火墙在安全体系方面的一个完善  
  它作用于同一内部子网之间的工作站与服务器之间，以确保内部网络服务器的安全。这样防火墙的作用不仅是用于内部与外部网之间的防护，还可应用于内部网各子网之间，同一内部子网工作站与服务之间。可以说达到了应用层的安全防护，比起网络层更加彻底。

* ##### 中心管理\(CeNT/2Kral ManagementNT/2K\)

  服务器软件，负责总体安全策略的策划、管理、分发和日志的汇总。具有以往防火墙所不具有的管理功能。

### 基本原理

由中心定义策略，但由各个分布在网络中的端点实施这些策略。  
依赖于三个主要概念  
说明哪一类连接可以被允许禁止的策略语言；  
一种系统管理工具；  
IP安全协议；

### 工作方式

![](/assets/66import.png)

### 特点

分布式防火墙负责对网络边界、各子网和网络内部各节点之间的安全防护，所以“分布式防火墙”是一个完整的系统，而不是单一的产品。

### 分布式防火墙的优势

* 增强的系统安全性
* 提高了系统性能
* 提高系统的可扩展性
* 实施主机策略
* 应用更为广泛，支持VPN通信


