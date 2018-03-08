# Zxw.Framework.NetCore
基于EF Core的Code First模式的DotNetCore快速开发框架

**开发环境**
* VS2017 / VS Code
* .net core 2.0

**支持的数据库**
* SQL Server
* MySQL
* Sqlite
* InMemory
* PostgreSQL


**缓存组件使用**

本项目采用的AOP中间件 ：[AspectCore-Framework](https://github.com/dotnetcore/AspectCore-Framework)
* MemoryCacheAttribute ：基于MemoryCache的缓存拦截组件
* RedisCacheAttribute ：基于Redis的缓存拦截组件

如何使用：

    public interface ITutorClassTypeRepository:IRepository<TutorClassType, Int32>
    {
        [MemoryCache]
        IList<TutorClassType> GetByMemoryCached(Expression<Func<TutorClassType, bool>> where = null);

        [RedisCache(Expiration = 5)]
        IList<TutorClassType> GetByRedisCached(Expression<Func<TutorClassType, bool>> where = null);
    }

**.net framework版本地址**

[Zxw.Framework.Nfx](https://github.com/VictorTzeng/Zxw.Framework.Nfx)



**项目说明**

请参考我的博客：[http://www.cnblogs.com/zengxw/p/7673952.html](http://www.cnblogs.com/zengxw/p/7673952.html)


# dev分支日志

**2018/1/14**

1.add bulkinsert for mysql

2.modify and test bulkinsert for mssql

 
**2017/12/26**

1.测试Redis
