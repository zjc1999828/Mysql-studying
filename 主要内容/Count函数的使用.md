# Count函数的使用
----
----
Count(*)与Count(字段)
![在这里插入图片描述](https://img-blog.csdnimg.cn/0588a8ae23074366aa4244235c032460.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)

```sql
SELECT * FROM score

SELECT COUNT(`name`)  FROM score WHERE math > 70

SELECT COUNT(*) FROM score WHERE math > 70
```

