# 项目说明

> 本项目为一款综合服务类App，包含用户话费充值，广告，新闻， 办卡， 商城， 社区等功能。

# 工作职责

> 担任公司架构组成员，职位是全栈架构师，因此参与业务较少，主要负责架构设计，疑难杂症问题解决，环境部署。

# 工作内容

1.独自一人负责公司前后端分离设计及前端拆分。

  >因业务扩展，平台需提供PC, Wap, APP多平台产品，之前的jsp服务端渲染设计已完全不能满足，因此需进行前后端拆分。
  
  >>前端架构设计需求：
  
     自定义脚手架，需支持vue和react,支持方便扩展，支持多入口，动态cdn,静态文件copy等
     集成国际化，路由，状态管理， 缓存，网络调用等基础功能，业务方只需配置即可。
     封装和开发核心组件，高阶组件, vue版需提供统一数据校验框架。
  >>前端技术选型：
  
      PC: 管理平台使用vue + iview, 用户： react + antd
      Wap: react + antd
      App: react native + 原生代码
  >>前端架构设计：
  
      1. 阅读vue-cli及react-scripts源码，提取二者的打包核心代码，基于webpack4重新开发脚手架。（easy-cli）
      2. 脚手架功能完善，支持多入口，动态cdn, 静态文件copy
      3. 开发vuePlugin用于vue核心功能封装（router, i18n, 核心组件， 核心mixins, vuex， cache, axios)，业务方只需安装vuePlugin,配置路由，i18n等即可
      4. 开发reactPlugin和reactNativePlugin, 封装核心功能（router, i18n, 核心组件， redux， cache, axios)
  >>疑难杂症排查：
  
      1. 解决reactNative的asyncStorage失效问题
      2. 解决wap网页被百度APP拦截问题
      3. react模块加载按需问题`
      
2.服务端工作内容：

    1.cache的AOP实现，只需在需要刷新缓存的service方法中添加@reflushCache注解即可， AOP在有该注解的方法体的AfterReturn中刷新对应缓存。
    2.tomcat自定义Valve实现并发数控制。
    3.服务端代码的spring boot改造，将老项目改造成spring boot版本。
    4.完成老项目的dubbo版本监控二次开发。（服务端将dubbo版本信息存储到redis中，监控中心从redis获取）
    5.协助业务人员解决开发中的各种问题。
    6.研究greenplumDataBase,并部署到docker中。（基于postgresql9.4版本，因官方未正式发布基于9.4版本的greenPlum,所以需要基于Master分支自己搭建，难度还是有的）