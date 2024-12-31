# onlinevideocoment
Java：189 基于SSM框架的在线电影评价系统
> #### 作者主页：[舒克日记](https://blog.csdn.net/cativen)
>
>  简介：Java领域优质创作者、Java项目、学习资料、技术互助
>
> <b><font color=red>文中获取源码</font></b>

# 项目介绍

系统的用户分管理员和用户两个角色的权限子模块。

管理员的主要功能：用户信息管理、管理员信息管理、电影信息管理、论坛信息管理、电影动态管理、投票信息管理。

用户的主要功能：对电影进行评价，投票，并可以换相留言讨论。可以查看最新的动态信息，以及论坛交流

# 环境要求

1.运行环境：最好是java jdk1.8,我们在这个平台上运行的。其他版本理论上也可以。

2.IDE环境：IDEA,Eclipse,Myeclipse都可以。推荐IDEA;

3.tomcat环境：Tomcat7.x,8.X,9.x版本均可

4.硬件环境：windows7/8/10 4G内存以上；或者Mac OS;

5.是否Maven项目：是；查看源码目录中是否包含pom.xml;若包含，则为maven项目，否则为非maven.项目

6.数据库：MySql5.7/8.0等版本均可；

# 技术栈

运行环境：jdk8 + tomcat9 + mysql5.7 + windows10

服务端技术：Java、Spring、SpringMVC、Mybatis，SSM

前端：jsp

# 使用说明

1.使用Navicati或者其它工具，在mysql中创建对应sq文件名称的数据库，并导入项目的sql文件；

2.使用IDEA/Eclipse/MyEclipse导入项目，修改配置，运行项目；

3.将项目中config-propertiesi配置文件中的数据库配置改为自己的配置，然后运行；

# 运行指导

idea导入源码空间站顶目教程说明(Vindows版)-ssm篇：

http://mtw.so/5MHvZq

源码地址：[http://www.codegym.top](http://www.codegym.top/)

# 运行截图

## 功能模块截图

![img](https://i-blog.csdnimg.cn/img_convert/eb78f3c68c976aa608861d68eaa78326.png)

![image20241219222020715](https://i-blog.csdnimg.cn/img_convert/b467afe1ce60126ddb2f1dec28e24e10.png)

#### 项目截图

前台

![1](https://i-blog.csdnimg.cn/img_convert/aa43e4e99338c05fc7dd490e901949d4.png)

![捕获](https://i-blog.csdnimg.cn/img_convert/8651f5f187baa8ee9d03646626c985b4.png)

![捕获2](https://i-blog.csdnimg.cn/img_convert/14f51514dec390a660858532d1612d9c.png)

![捕获22](https://i-blog.csdnimg.cn/img_convert/d6cb9c718d0f81f47209d54dc313cb9d.png)

后台

![b7a1f68937a64a849960050b57e54812](https://i-blog.csdnimg.cn/img_convert/2fe96a84e11c26ffe41bd974174d9f75.png)

![c702e39c9c774d59b381b4737acca04e](https://i-blog.csdnimg.cn/img_convert/e10fef235346378f1c0b5cf03b786a07.png)

### 代码

```
    public static long getThirtyDaysMillisFromLocalDate(Long days) {
        // 获取当前日期
        LocalDate today = LocalDate.now();
        LocalDate thirtyDaysAgo = today.minusDays(days);
        // 将 LocalDate 转换为系统默认时区的 ZonedDateTime（午夜）
        ZonedDateTime zonedDateTime = thirtyDaysAgo.atStartOfDay(ZoneId.systemDefault());
        // 将 ZonedDateTime 转换为 Instant，并获取毫秒数
        Instant instant = zonedDateTime.toInstant();
        return instant.toEpochMilli();
    }
```
