

<h1 align="center">MallChat</h1>
<p align="center"><strong>一个既能购物又能即时聊天的电商系统。<br>电商该有的购物车、订单、支付、推荐、搜索、拉新、促活、推送、物流、客服、它都必须有。</strong></p>

### 项目介绍

MallChat是一个IM项目，通过netty实现和前端的websocket连接。内含微信扫描登录，成员列表，消息列表，消息互动，丰富的消息类型，还有很多实用的小轮子列如aop日志，分布式锁注解，频控注解，ip解析归属地等。

### 项目启动及部署

- 环境: node 16.18+, 包管理工具 pnpm (安装完 node 执行 `npm i pnpm -g` 即可);
- 安装依赖: clone 工程之后，执行 `pnpm i`
  - `npm` 安装报错, 命令后加参数 `npm i --ignore-scripts` 忽略 `scripts` 相关依赖即可解决
    ![p9211Ag.png](https://s1.ax1x.com/2023/08/25/pPNP6RU.png)
  - 推荐使用 `pnpm`, 安装依赖不会有 因为网络而失败 的问题
- 启动: 按 `F5` 即可自动执行 `pnpm run dev` 并且打开浏览器
- 部署
  - 部署到本地：执行 `pnpm build` 构建完成后把 `dist` 文件夹 放到服务器，并配置 `nginx` 即可

### 后端环境搭建

在项目目录下的`application.yml`修改自己的启动环境`spring.profiles.active` = `test`然后找到同级文件`application-test.properties`，填写自己的环境配置。

### 技术选型

#### 后端技术

|        技术         | 说明                                       | 官网                                                         |
| :-----------------: | ------------------------------------------ | ------------------------------------------------------------ |
|     SpringBoot      | web开发必备框架                            | [https://spring.io/projects/spring-boot](https://spring.io/projects/spring-boot) |
|       MyBatis       | ORM框架                                    | http://www.mybatis.org/mybatis-3/zh/index.html               |
|     MyBatisPlus     | 零sql，简化数据库操作，分页插件            | [https://baomidou.com/](https://baomidou.com/)               |
|        Redis        | 缓存加速，多数据结构支持业务功能           | [https://redis.io](https://redis.io)                         |
|      Caffeine       | 本地缓存                                   | http://caffe.berkeleyvision.org/                             |
|        Nginx        | 负载均衡，https配置，websocket升级，ip频控 | [https://nginx.org](https://nginx.org)                       |
|       Docker        | 应用容器引擎                               | [https://www.docker.com](https://www.docker.com)             |
|         Oss         | 对象存储                                   | [https://letsencrypt.org/](https://letsencrypt.org/)         |
|         Jwt         | 用户登录，认证方案                         | [https://jwt.io](https://jwt.io)                             |
|       Lombok        | 简化代码                                   | [https://projectlombok.org](https://projectlombok.org)       |
|       Hutool        | Java工具类库                               | https://github.com/looly/hutool                              |
|     Swagger-UI      | API文档生成工具                            | https://github.com/swagger-api/swagger-ui                    |
| Hibernate-validator | 接口校验框架                               | [hibernate.org/validator/](hibernate.org/validator/)         |
|        minio        | 自建对象存储                               | https://github.com/minio/minio                               |

#### 前端技术

|     技术     | 说明                                      | 官网                                                         |
| :----------: | ----------------------------------------- | ------------------------------------------------------------ |
|     Vue3     | 前端流行开发框架                          | [https://cn.vuejs.org](https://cn.vuejs.org)                 |
|    Pinia     | vue3 官方推荐状态管理框架                 | [https://pinia.vuejs.org](https://pinia.vuejs.org)           |
|  vue-router  | Vue 的官方路由                            | [https://router.vuejs.org](https://router.vuejs.org)         |
|  TypeScript  | 让 JS 具备类型声明                        | https://www.typescriptlang.org/                              |
| Element Plus | 缓基于 vue3 的组件库                      | [https://element-plus.gitee.io](https://element-plus.gitee.io) |
|    Alova     | 轻量级的请求策略库，用起来负担比 axios 小 | https://alova.js.org/                                        |
|     vite     | 极速的前端打包构建工具                    | [https://cn.vitejs.dev](https://cn.vitejs.dev)               |
|     pnpm     | 速度快、节省磁盘空间的软件包管理器        | [https://www.pnpm.cn](https://www.pnpm.cn)                   |

