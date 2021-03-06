# 数字签名的原理

利用公钥密码技术实现数字签名

### 完整的数字签名过程

* #### 签名

  ![](/assets/signature.png)

* #### 鉴别

  ![](/assets/verify.png)

##### 存在的问题：

由于知道发送者身份的人都可以获得公钥PKA，因此，除真正的接收方B以外，其他截取信息的人也可以知道明文的真实内容

### 保密性的数字签名：

![](/assets/imddport.png)

利用双重公私钥加密/解密机制，可以实现信息通信的保密性和数字签名

##### 存在的问题:

1. 加/解密效率不理想
2. 不能确保信息的完整性？？

### 基于“数字指纹”的解决方案

数字签名的对象不是传送信息本身，而是该信息的信息摘要（即“数字指纹”）

典型消息摘要算法：MD5，SHA等

在保证数字签名和通信安全性的前提下，提高加/解密执行效率

#### 步骤

1. 发送方使用单向散列算法对原始信息进行计算，获得一个固定长度的信息摘要
2. 发送方用自己的私钥加密生成的信息
   1. 生成发送方的数字签名
3. 发送方把这个数字签名作为发送信息的附件和明文信息，一同用接收方的公钥进行加密，将加密后的密文一同发送给接收方；
4. 接收方首先把接收到的密文用自己的私钥解密，得到明文信息和数字签名，再用发送方的公钥对数字签名进行解密，然后使用相同的单向散列算法来计算解密得到的明文信息，得到信息摘要；
5. 对比计算出来的信息摘要和发送方发送过来的信息摘要是否一致
   1. 一致：数字签名的确是发送方的
   2. 不一致：收到的信息是伪造的或被篡改过。

### 数字签名的分类

* 直接方式的数字签名  
  只有通信双方参与，假定接收方知道发送方的公钥

  * 保密方式
    * 外部保密方式（对需要签名的信息进行数字签名）
    * 内部保密方式（对已加密的信息进行数字签名）
      * 解决争议时，需要提供信息的解密密钥
  * 存在的问题
    * 方案的有效性取决与发送方密钥的安全性
      * 防止发送方抵赖（比如声称自己的私钥丢失或被盗）
      * 窃取发送方私钥，伪造时间戳，伪造签名

* 具有仲裁方式的数字签名

  * 运行方式
    * 发送方对发往接收方B的信息签名后，将信息及其签名先发送给仲裁者C，C对信息及其签名验证完成后，再连同一个表示已通过验证的指令一起发送给接收方B。由于C的存在，A无法对自己发出的信息予以否认。
    * 仲裁者起到非常重要的作用，应取得所有用户的信任
  * 存在的问题
    * 仲裁者的处理能力成为系统技术瓶颈



