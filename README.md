# NewsInfo
Intellij IDEA + Maven + Spring Boot + Scala + Velocity + Boostrap + jQuery
1.	使用idea工具创建springboot项目  选择web,mybatis,mysql等选项
2.	使用mysqlworkbench查看数据库
3.	使用view Object向页面传递参数  一个Map<String.Object>  和对map的get,set方法
4.	通过注解的方式配置mybatis 数据库增删改查
5.	根据时间分组展示   
6.	注册时密码使用 普通密码加uuid的五位  在进行MD5加密
7.	使用alibaba-fastjson进行json封装
8.	登陆时设有过期时间(防止别人捕获持有)  登陆状态LoginTicket一张表关联用户表
9.	1. HTTPS注册页 2. 公钥加密私钥解密，支付宝h5页面的支付密码加密 3. 用户密码salt防止破解（CSDN，网易邮箱未加密密码泄漏） 4. token有效期 5. 单一平台的单点登陆，登陆IP异常检验 6. 用户状态的权限判断 7. 添加验证码机制，防止爆破和批量注册
10.	使用postman进行网页调试与发送网页http请求测试
11.	阿里云存储  七牛云存储(对学生免费)
12.用户的登录(带有token令牌)和注册(密码使用salt和MD5加密):
    1.token关联用户id,并将token存储至cookie中,设置过期时间(过期用户将再次输入密码会更新token
    2.客户端发送带token的HTTP请求,服务的从token获取id并获取用户具体信息和权限. 
13.使用redis实现点赞功能: 
    1.mysql设计部分:post_like记录文章被赞的次数 user_like_post记录用户记录过哪些文章
    2.redis设计部分:post_set存放被点赞文章 post_user_like_set_{$post_id}以post_id为key,存储对该post点 赞的用户        post_user_like_{$post_id}_{user_id}对每个用户对该post点赞的情况存入hash中post_{$post_id}_counter 记录点赞数,只记录未同步的点赞数)
