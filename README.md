SLFMDBUtil
==========
FMDB查询及结果集封装，依赖FMDB框架和sqlite3，使用时请导入这两个框架。
    
使用方法：
==========
###1.使用前先修改自己的数据库名和创建表的SQL语句，修改位置如下：
在SLFMDBUtil.h中的initialize方法中修改数据库名称，在SLFMDBUtil.h中的loadDatabas方法中修改创建表的SQL语句。
###2.校验SQL语句是否正确：
    BOOL isValid = [SLFMDBUtil executeStatements:sql];
###3.执行SQL查询语句：
    SLResultSet *rs = [SLFMDBUtil executeQuery:sql, ...];
    或
    SLResultSet *rs = [SLFMDBUtil executeQuery:sql withArgumentsInArray:params];
###4.执行SQL更新语句：
    BOOL isSuccess = [SLFMDBUtil executeUpdate:sql, ...];
    或
    BOOL isSuccess = [SLFMDBUtil executeUpdate:sql withArgumentsInArray:params];
###5.得到结果集的总行数
    SLResultSet *rs = [SLFMDBUtil executeQuery:sql];
    NSUInteger rowCount = [rs rowCount];
###6.得到结果集的总列数
    SLResultSet *rs = [SLFMDBUtil executeQuery:sql];
    NSUInteger columnCount = [rs columnCount];
###7.结果集是否有下一行
    SLResultSet *rs = [SLFMDBUtil executeQuery:sql];
    if ([rs next]) {
        
    }
