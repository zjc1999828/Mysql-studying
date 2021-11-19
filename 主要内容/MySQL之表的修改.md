# MySQL之表的修改
----
----

```sql
-- 在resume后面增加一列字段image
ALTER TABLE emp 
ADD image VARCHAR(32) NOT NULL DEFAULT ''
AFTER RESUME


-- 修改字段job的长度为60个字符
ALTER TABLE emp
MODIFY job VARCHAR(60)NOT NULL DEFAULT ''

-- 删除sex字段
ALTER TABLE emp
DROP sex

-- 修改表名
RENAME TABLE emp TO employee

-- 修改表的字符集为utf8
ALTER TABLE employee 
CHARACTER SET utf8

-- 字段名修改
ALTER TABLE employee 
CHANGE `name` user_name VARCHAR(32)NOT NULL DEFAULT ''

-- 显示所有字段的信息
DESC employee
```

