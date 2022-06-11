## MongoDB

#### 连接地址：

http://127.0.0.1:27017/

#### 查看版本：

```sql
$ mongod -version
```

#### 查看安装路径：

```sql
$ which mongod
```

#### 启动服务：

```sql
$ sudo mongod --config /usr/local/etc/mongod.conf
```

#### 查看服务是否启动：

```sql
$ ps aux | grep -v grep | grep mongod
```

#### 停止服务：

```sql
$ mongo # 打开终端
$ use admin # 切换用户
$ db.shutdownServer() # 关闭
```

#### 相关终端：

```sql
$ mongo # 打开终端
$ exit # 关闭终端
```

#### 建立数据库：

```sql
$ use db
```

> use 不仅可以进入一个数据库，如果你敲入的库不存在，它还可以帮你建立一个库。但是在没有集合前，它还是默认为空。

#### 新建数据集合和插入文件（数据）

```sql
$ db.集合.insert()
```

> - 新建数据集合和插入文件（数据），当集合没有时，这时候就可以新建一个集合，并向里边插入数据。
> - Demo : db.user.insert({“name”:”jspang”})

#### 查询所有数据

```sql
$ db.集合.find()
```

> - 这条命令会列出集合下的所有数据，可以看到 MongoDB 是自动给我们加入了索引值的。
> - Demo : db.user.find()

#### 查询第一个文件数据

```sql
$ db.集合.findOne()
```

> 所有 MongoDB 的组合单词都使用首字母小写的驼峰式写法。

#### 修改数据

```sql
$ db.集合.update({查询},{修改})
```

> - 第一个是查询条件，第二个是要修改成的值。
> - Demo : db.jspang.update({"name":"jspang"},{"name":"jspang","age":"32"})

#### 删除文件数据

```sql
$ db.集合.remove(条件)
```

> - 注意的是要跟一个条件。
> - Demo : db.user.remove({“name”:”jspang”})

#### 删除整个集合

```sql
$ db.集合.drop()
```

#### 删除整个数据库

```sql
$ db.dropDatabase()
```
