SLFMDBUtil
==========
FMDB查询及结果集封装

使用方法：
==========
###1. 使用前先修改自己的数据库名和创建表的SQL语句，修改位置如下：
在SLFMDBUtil.h中的initialize方法中修改数据库名称，在SLFMDBUtil.h中的loadDatabas方法中修改创建表的SQL语句。
###2. 校验SQL语句是否正确：
    BOOL isValid = [SLFMDBUtil executeStatements:sql];
###3. 执行SQL查询语句：
    SLResultSet rs = [SLFMDBUtil executeQuery:sql, ...];
    或
    SLResultSet rs = [SLFMDBUtil executeQuery:sql withArgumentsInArray:params];
###4. 执行SQL更新语句：
    BOOL isSuccess = [SLFMDBUtil executeUpdate:sql, ...];
    或
    BOOL isSuccess = [SLFMDBUtil executeUpdate:sql withArgumentsInArray:params]; 
