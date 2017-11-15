# 访问控制技术

#### 两个基本理论模型

* ##### 引用监控器\(Reference Monitor\)

  ![](/assets/3import.png)   
  访问控制依赖引用监控器进行主体对客体访问的控制，以决定主体是否有权对客体进行操作和进行何种操作。引用监控器查询授权数据库\(Authorization Database\)，根据系统安全策略进行访问控制的判断，同时将相应活动记录在审计数据库\(Audit Database\)中。

* ##### 访问矩阵\(Access Matrix\)

  ![](/assets/4import.png)   
  访问矩阵模型描述了访问控制策略。 在访问矩阵模型中，系统的状态由三元组\(S,O,A\)来定义 S是主体的集合——行标对应主体 O是客体的集合——列标对应客体 A是访问矩阵，矩阵元素A\[s,o\]是主体s在o上实施的操作 客体以及在其上实施的操作类型取决应用系统本身的特点

  * 实际应用中实现访问矩阵的三种方法
    * 访问控制列表\(Access Control List，ACL\)
    * 能力列表\(Capability List\)
    * 授权表\(Authorization Table\)



