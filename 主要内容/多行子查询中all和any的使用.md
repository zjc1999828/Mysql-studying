# 多行子查询中all和any的使用
----
----


all的练习

![在这里插入图片描述](https://img-blog.csdnimg.cn/446c1461ff84455989936b59c6f5fe73.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)


```sql
SELECT ename,job,deptno 
FROM emp 
WHERE sal > (SELECT MAX(sal) FROM emp WHERE deptno = 30)


SELECT ename,job,deptno 
FROM emp 
WHERE sal >ALL(SELECT sal FROM emp WHERE deptno = 30)
```


any的练习

![在这里插入图片描述](https://img-blog.csdnimg.cn/e26dbc78560d4a9a9e44f237b8793af1.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)

```sql

SELECT ename,job,deptno 
FROM emp 
WHERE sal > (SELECT MIN(sal) FROM emp WHERE deptno = 30)


SELECT ename,job,deptno 
FROM emp 
WHERE sal >ANY(SELECT sal FROM emp WHERE deptno = 30)
```

