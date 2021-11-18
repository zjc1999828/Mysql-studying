# MySQL数据库常用SQL语句
----
----
##### 创建数据库
create database ___character set __ collate _

##### 删除数据库
drop database

![在这里插入图片描述](https://img-blog.csdnimg.cn/8519ab87fcb34323bf0eeeb772a7b3ec.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)
![在这里插入图片描述](https://img-blog.csdnimg.cn/a147249aa41d4a909d5f290c65f3dd1c.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)

##### 显示所有数据库
show databases

##### 查看之前创建数据库的定义信息
show create database ___
![在这里插入图片描述](https://img-blog.csdnimg.cn/bb5876f95042443a88f122ea66b6002d.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)

##### 备份数据库
mysqldump -u root -pzjc -B 
##### 恢复数据库
一定要先进入MySQL命令行：使用(mysql - u root -pzjc)进入mysql命令行
source bak.sql

![在这里插入图片描述](https://img-blog.csdnimg.cn/ab89d7830bc94404bd24d97e26e6da82.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)
![在这里插入图片描述](https://img-blog.csdnimg.cn/ed780106c1f64a48828bf5535aebfb18.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)



恢复数据库第二种方法：复制粘贴bak.sql中的语句到SQLyog中执行即可。


##### 备份数据库中的表
![在这里插入图片描述](https://img-blog.csdnimg.cn/bff17e0aee3b4f058ce8ec1d72ee5a8d.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)

