

 学生管理系统：ASP.NetCore3.1 + Vue + EleUI
 
 > PS：当前版本只是我的一个练手项目，并不是商业化产品，在多表的处理上，没有用到mapper联查，而是所有数据都查出来，这种方式数据多了肯定会慢(当然，如果start100+，证明有人用，我会升级改造的)，所以目前大家不用过多的关注性能问题，主要是**业务逻辑的梳理**；  

 ### 操作流程

 
 
 #### 后端：  
 直接F5运行项目；

   
     
     
#### 前端：  
先`npm i`安装依赖包，然后直接运行即可。
 
          


 
 
 
 ### 整体框架设计
 
 #### 后端  	`Student.Achieve.Api` 为 `Blog.Core`  项目的迷你精简版，功能很少：
 ```
 0、ASP.NET Core 3.1 
 1、（展示层 + 仓储 + 接口）的分层设计；
 2、使用SqlSugar ORM 并初始化DB数据；
 3、Automapper 实现对象映射；
 4、CORS 实现跨域（用来支持IIS部署）；
 5、Swagger 提供文档说明；
 6、JWT 实现自定义策略授权认证；
 7、Autofac 作为依赖注入容器，提供程序集批量注册；
 8、支持上传 Excel 做数据导入；
 9、Log4net 负责日志处理；
 10、成绩可视化；
 ```

 

 ### 前端  	`Student.Achieve.UI` 为 `Blog.Admin`  项目的使用版本，有一定的出入：
 ```
 0、Vue 2 + Ele UI
 1、Router 路由
 2、Axios 数据请求；
 3、Automapper 实现对象映射；
 4、动态路由 + 导航条；
 5、提供上传功能；
 6、JWT 实现自定义策略授权认证；
 7、Autofac 作为依赖注入容器，提供程序集批量注册；
 8、支持上传 Excel 做数据导入；
 9、核心的还是教学教务系统：学生+教师管理、课程管理、授课管理、考试管理、成绩管理等等（start数超过100+，我可以录个视频吧，因为比较简单，其实看看对应的实体类就能看懂）
 ```
 

### 主要页面

![img](http://img.neters.club/github/640.png)
![img](http://img.neters.club/github/33.png)
