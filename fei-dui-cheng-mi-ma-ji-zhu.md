# 非对称密码技术

> 1976年，美国学者Diffie和Hellman发表了著名论文《密码学的新方向》，提出了建立“公开密钥密码体制”
>
> 目前世界上用得最多的公钥密码算法是**RSA**、**离散对数**和**ECC**。

若用户A有加密密钥ka（公开），不同于解秘密钥ka’（保密），要求ka的公开不影响ka’的安全。  
若B要向A保密送去明文m,可查A的公开密钥ka，若用ka加密得密文c，A收到c后，用只有A自己才掌握的解密密钥ka’对x进行解密得到m。

### 优点

* ##### 密钥分发简单

  由于加密密钥与解密密钥不能互推，使得加密密钥表可以像电话号码本一样由主管部门发给各个用户。

* ##### 需要秘密保存的密钥量少

  网络中每个成员只需秘密保存自己的解密密钥，N个成员只需产生N对密钥

* ##### 互不相识的人之间也能进行保密对话

  一方只要用对方的公开密钥加密发出，收方即用自己密藏的私钥解密，而任何第三方即使知道加密密钥也无法对密文进行解密。

* ##### 可以进行数字签名

  发信者用他的秘密密钥进行签名，收信者可用发信者的公钥进行验证。

### 缺点

* ##### 执行效率低

  比同等强度的对称密码技术要慢10倍——100

* ##### 密文不紧凑

  非对称加密得到的密文长度大于最初的明文长度  
  多重非对称加密中，这个问题更严重

### 意义

* ##### 解决大规模网络应用中密钥的分发和管理问题

  * ###### 需要管理的秘密密钥数量大大减少

    采用公钥密码体制，N个用户只需要产生N对密钥。以100万个用户为例，只需100万对密钥，需要秘密保存的仅100万个私钥。而利用传统密码体制，为保证不被第三方窃听，需要N（N–1）/2=4950万个密钥！

  * ###### 分发简单，安全性好

    公钥密码加密密钥通常是公开的，而解密密钥是秘密的，由用户自己保存，不需要往返交换和传递减少了密钥泄露的危险性
* ##### 实现网络中的数字签名机制

  * 数字签名的数据需要有惟一性、私有性，而对称密钥技术中的密钥至少需要在交互双方之间共享，因此，不满足惟一性、私有性，无法用做网络中的数字签名。

  * 公钥密码技术由于存在一对公钥和私钥，私钥可以表征惟一性和私有性，而且经私钥加密的数据只能用与之对应的公钥来验证，其他人无法仿冒，所以，可以用做网络中的数字签名服务。



