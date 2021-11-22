# 分组查询中的顺序
--------
---------

![在这里插入图片描述](https://img-blog.csdnimg.cn/39e9828dc79e49e69dcc302839e7bfd1.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)
![在这里插入图片描述](https://img-blog.csdnimg.cn/60513537533040d7b258a4e53d33696e.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)

```sql
SELECT deptno,AVG(sal) AS 平均工资 FROM emp 
GROUP BY deptno HAVING 平均工资>1000 
ORDER BY 平均工资 DESC 
LIMIT 0,2;
```

