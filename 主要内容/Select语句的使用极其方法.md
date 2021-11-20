# Select语句的使用极其方法
----
-----
![在这里插入图片描述](https://img-blog.csdnimg.cn/461982fbf4754c098f778bbcee1a4c75.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)
![在这里插入图片描述](https://img-blog.csdnimg.cn/922f2bb73d1e44a18335307e4391c5d3.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)

##### as语句的使用
![在这里插入图片描述](https://img-blog.csdnimg.cn/7f135597a1f749d6a504bd451d349b88.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)





##### where子句在select中的使用
![在这里插入图片描述](https://img-blog.csdnimg.cn/cfb6b8e4baff45bda134552749c2c66f.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)

```sql
SELECT * FROM score;

SELECT * FROM score WHERE math > 60 OR id > 4;

SELECT * FROM score WHERE math > chinese;

SELECT * FROM score WHERE (chinese+math+english)>200 AND math < chinese AND `name` LIKE '赵%'-- %表示模糊查询


SELECT * FROM score WHERE math BETWEEN 80 AND 90;-- between and 是闭区间

SELECT * FROM score WHERE math IN(89,90,91)

SELECT * FROM score WHERE `name` LIKE '韩%'
```


##### order by 语句的使用

==order by语句一定要放在每个select语句的最后，因为order by 是最后的条件了，即所有的查询条件都执行完了，数据都被找到了之后，最后决定如何输出的一步语句，所以放在最后==
![在这里插入图片描述](https://img-blog.csdnimg.cn/1f3777827c494da2b08547efb9451fc1.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)

```sql
SELECT * FROM score ORDER BY math ASC

SELECT * FROM score WHERE `name` LIKE '韩%' ORDER BY (chinese + english + math )ASC

SELECT `name`,(chinese + english + math) AS total_score FROM score ORDER BY total_score DESC
```

