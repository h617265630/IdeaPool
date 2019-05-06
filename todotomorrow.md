配置 php项目  third party



# 连接redis报此错误：ERR Client sent AUTH, but no password is set

2016年12月25日 11:58:42

[lys07962000](https://me.csdn.net/lys07962000)

阅读数：17618

from:

http://bbs.csdn.net/topics/391824759?page=1  


  


127.0.0.1:6379&gt; auth 123456  
ERR Client sent AUTH, but no password is set  


设置其密码

redis 127.0.0.1:6379&gt; CONFIG SET requirepass "123456"  
OK  
redis 127.0.0.1:6379&gt; AUTH 123456  
Ok  
  
设置下这个配置密码就好了

注意事项: php版本问题

配置 nodejs 项目

连接 pg数据库

修改 积分报表的bug

开始使用pg数据库 ，先从一张报表开始。

