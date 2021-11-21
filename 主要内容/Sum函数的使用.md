# Sum函数的使用
----
----


![在这里插入图片描述](https://img-blog.csdnimg.cn/b7f03530af0a41799b47c34cb426bd4b.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)





```sql
SELECT SUM(math) AS 数学总成绩 FROM score

SELECT  SUM(math)+SUM(english)+SUM(chinese) AS 总分 FROM score


SELECT  (SUM(math)+SUM(english)+SUM(chinese))/COUNT(*) AS 平均分 FROM score
```

