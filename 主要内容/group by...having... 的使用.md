# group by...having... 的使用
----
----

![在这里插入图片描述](https://img-blog.csdnimg.cn/465dcfe44f2843269c2f811e9a7c4cbe.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)
![在这里插入图片描述](https://img-blog.csdnimg.cn/6a3e5ce1654e455d831198ed410ebbe3.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)


==例子：==
![在这里插入图片描述](https://img-blog.csdnimg.cn/ae017d63a60f4c09826ea4c57af38eb3.png)

```sql
-- 显示每个部门的最高工资和平均工资
SELECT MAX(sal) AS 该部门的最高工资 ,AVG(sal) AS 该部门的平均工资 ,deptno
FROM emp 
GROUP BY deptno

-- 显示每个部门的每种岗位的最高工资和平均工资
SELECT MAX(sal) AS 该部门的最高工资 ,AVG(sal) AS 该部门的平均工资 ,deptno,job 
FROM emp 
GROUP BY deptno,job


-- 显示平均工资低于2000的部门，以及这个部门的平均工资

SELECT  deptno , AVG(sal) AS 平均工资 FROM emp  GROUP BY deptno HAVING  平均工资 < 2000
```

