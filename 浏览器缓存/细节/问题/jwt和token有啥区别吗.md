### jwt和token有啥区别吗?

**相同：**

- 都是访问资源的令牌

- 都可以记录用户的信息

- 都是使服务端无状态化

- 都是只有验证成功后，客户端才能访问服务端上受保护的资源

**区别：**

- Token：服务端验证客户端发送过来的 Token 时，还需要查询数据库获取用户信息，然后验证 Token 是否有效。

- JWT： 将 Token 和 Payload 加密后存储于客户端，服务端只需要使用密钥解密进行校验（校验也是 JWT 自己实现的）即可，不需要查询或者减少查询数据库，因为 JWT 自包含了用户信息和加密的数据。