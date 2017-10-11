* 由密钥分配中心KDC，或者由一组节点组成层次结构负责密钥的产生并分配给通信双方。
* 用户不需要保存大量的会话密钥，只需要保存同KDC通信的加密密钥
* 通信量大，要求具有较好的鉴别功能以鉴别KDC和通信方

在网络中用户太多，且地域分布很广的情况下，一个KDC无法负担所有用户的密钥分配任务，解决方案：
采用分层KDC结构。根据用户数目及分布，建立两层或多层KDC。




