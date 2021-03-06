# 安全审计

不具有强有力的安全审计支持的网络，其安全性无从谈起

### 安全审计的基本要求

审计信息必须被有选择地保留和保护，与安全有关的活动能够被追溯到负责方，系统应能够选择那些与安全有关的信息并被记录，以便将审计的开销降低到最小，从而可以进行有效的分析。

### 在C2等级中，审计系统必须实现的功能

系统能够创建和维护审计数据，保证审计记录不能被删除、修改和非法访问

### 目前网络安全审计的形势

认识到安全审计的重要性，但在对安全审计概念的确切理解上存在差别

标准上的不统一导致目前安全审计产品市场上鱼龙混杂

### 当前安全审计类产品情况

* ##### 网络设备及防火墙日志

通常具备一定的日志功能

###### 存在的不足

受网络设备和防火墙分析能力的限制，目前只能记录自身运转情况和一些简单的违规信息，不能提供具体有价值的网络操作信息；

往往采用内存记录日志，空间有限，有用信息容易被覆盖，而且信息不能做永久保存

——与安全审计的要求相差甚远

* ##### 操作系统日志

  一般都提供日志功能，记录一些零碎信息  
  存在的问题  
  无法理解用户具体操作行为，难以获得整个入侵过程的完整信息；  
  对分布式入侵分析效率不高；  
  无法对发生的攻击采取及时的响应，一旦日志文件被篡改，日志文件中信息的准确性不能保证  
  ——与安全审计的要求相差甚远

* ##### 侦听类工具

  能够获得网络上流过的数据包信息，能够观察到网络用户的操作和传输的数据，有利于对违规事件的检测  
  存在的问题  
  分析能力不足  
  不具备关联分析能力  
  缺乏报警响应能力  
  大量无用的冗余信息  
  ——不满足安全审计的要求

### 安全审计的技术实现基础

目前，计算机网络应用的趋势是开放型的网络协议和开放型的平台，网络上的任何应用（包括入侵和违规行为）都必须遵循相同的协议标准，因此这些操作在穿越网络时会留下一定的踪迹（构成了安全审计的对象）

### 网络安全审计系统的基本原理

对于这些行为进行分析、识别和判断，并完整记录

