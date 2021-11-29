# JDBC中批处理的应用
----
----

```sql
                preparedStatement.setInt(1,i);
                preparedStatement.setString(2,"zjc"+i);
                preparedStatement.addBatch();
```

```sql
            preparedStatement.executeBatch();
            preparedStatement.clearBatch();
            connection.commit(); //事物提交
```

![在这里插入图片描述](https://img-blog.csdnimg.cn/15ede6c943b341e69b584dd8f1933e5d.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)
![在这里插入图片描述](https://img-blog.csdnimg.cn/3d77ffe93c394886bb669746f90d2e97.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)

```sql

public class zzz {
    public static void main(String[] args)  {
        Connection connection = null;
        PreparedStatement preparedStatement = null;
        ResultSet resultSet = null;
        int i = 0;
        try {
            String sql = "insert into jdbc values(?,?)";
            connection = JDBCUtils.getConnection();
            connection.setAutoCommit(false);//开启事物，设置自动提交为false。
            preparedStatement = connection.prepareStatement(sql);
            while(i < 5000){
                preparedStatement.setInt(1,i);
                preparedStatement.setString(2,"zjc"+i);
                preparedStatement.addBatch();
                 i ++;
            }
            preparedStatement.executeBatch();
            preparedStatement.clearBatch();
            connection.commit(); //事物提交
        } catch (Exception E) {
            E.printStackTrace();
        } finally {
            JDBCUtils.close(resultSet,preparedStatement,connection);
        }

    }
}

```

