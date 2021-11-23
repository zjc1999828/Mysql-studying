
# order by 语句的使用

==order by语句一定要放在每个select语句的最后，因为order by 是最后的条件了，即所有的查询条件都执行完了，数据都被找到了之后，最后决定如何输出的一步语句，所以放在最后==
![在这里插入图片描述](https://img-blog.csdnimg.cn/1f3777827c494da2b08547efb9451fc1.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)

```sql
SELECT * FROM score ORDER BY math ASC

SELECT * FROM score WHERE `name` LIKE '韩%' ORDER BY (chinese + english + math )ASC

SELECT `name`,(chinese + english + math) AS total_score FROM score ORDER BY total_score DESC
```

