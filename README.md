#### 0.说在前面的废话
yf指的是yfsoft，我常用的id的简写，在我心中这是一个牛x的组织（虽然现在就我一个人），我将全部的生命和精力投入在里面，愿意为之付出一切，而我的一切都属于它。

#### 1.它是什么？
**yf-api** 是近一年时间打磨出来的产品，简单的说就是可以快速简单的搭建一个http服务，建立在已有的业务数据之上，关联上数据库之后就自带了基本的CRUD的操作，并提供单一统一的服务接口，同步所有的终端数据流，能应对较大并发的请求和一些恶意的攻击，提供nodejs，angularjs，java，.net，php的sdk实现，最大程度的降低客户端集成api服务的成本。
###### 相应的产品列表：
###### a.服务端产品
* yf-fast-dbm 
持久层操作框架源码 [>>我是地址](https://github.com/yfsoftcom/yf-fast-dbm)

* yf-api-server 
服务端框架源码 [>>我是地址](https://github.com/yfsoftcom/yf-api-server)

* yf-demo-api 
demo项目[>>我是地址](https://github.com/yfsoftcom/yf-demo-api)

* yf-ci-web 
辅助工具，web端执行shell命令 [>>我是地址](https://github.com/yfsoftcom/yf-ci-web)
* yf-job-scheduler 
辅助工具，web端管理定时任务 [>>我是地址](https://github.com/yfsoftcom/yf-job-scheduler)

###### b.客户端产品（编码已完成，正在更新文档）
* ngapi
 angularjs前端SDK

* apiengine 
nodejs SDK

* apiengine4j
java SDK

* apiengine4net
.net SDK

* apiengine4php
php SDK



###### 1.1. 唯快不破
>业务实现速度和系统服务的响应速度都想快。这是每一个非技术的创始人的诉求。

* 持续部署
* 持续集成 
* 持续交付

这些很灵活的开发模式可以满足，但是想要在一个规模还不是很大的团队里实践这些东西，管理和实施成本太高，如何能应对这样的窘境？
技术选型很重要，在这点上花了很长的时间，决定用nodejs，因为它的事件驱动可以满足高并发，源码开源，社区活跃，大公司应用广泛，加之本身javascript的语法也已经比较简单，学习成本不高。

###### 1.2. 适应场景
* 专注前期创业或者做产品的小团队或者个人
* 没有全职后端开发的团队
* 前期没有很多资源投入到技术基础搭建上的团队
* 不使用云存储平台(如: parse 或者 leancloud) 的企业
* 现有系统是基于关系型数据库，想快速搭建api服务的团队

###### 1.3. 优势
* 完全开源，且在持续维护
* 代码量极少
>越少的代码，意味着出bug的概率越小
* 创作团队都健在
>创作团队特别闷骚，喜欢健身，还能活好久~~随时都能联系上
* 丰富的文档和实例代码
* 丰富的已经实现的SDK

#### 2. 为何用它
开发者的体验非常重要，同时开发者的效率也很重要，没有大牛，如何能尽快的做出产品？那么多端口要维护，团队是要效益的，投入产出比很重要。
让编码平台统一化、标准化、流程化才是提高产品输出效率，保证代码质量的正确姿势；
试问：
* 如何才能正确评估一个技术的工作量
* 如何能避免一些隐藏的大坑
* 如何能减少技术人员流失的风险
* 如何能缩短新员工上手的教学成本
* 如何能定义标准的入职技能评估
* 如何如何...
作为一个非技术驱动的团队来说，这些问题都是非常头疼的，能解决这些问题的人很难找到。
通过高薪吸引过来的人才是否能完全适合目前的团队？这些问题都是会影响到整个团队最终的归属的！可能一步就决定了产品的生死。

#### 3. 如何用它
* 备份并导出您的数据库
* 安装一台linux（推荐Centos）
* 安装好lnmp
* 上传 yfci 脚本
* 执行安装命令
* 导入您的数据库
* 配置数据库链接信息
* 执行部署命令
* 客户端配置sdk，参照示例完成开发集成

##### 3.1 开发流程
* 代码版本管理流程 ： git flow
* 基本架构管理流程 ： 前后端完全分离，业务全在后端完成，前端只负责交互
* 服务端开发管理流程 ： 根据已有开发框架做适配，JAVA、PHP、ASP.NET 都支持
* 客户端开发管理流程 ： 配置相应的客户端SDK，参照文档进行配置和使用即可

##### 3.2 版本发布流程
* 代码经过测试推入到Git服务器，通过平台的CI脚本进行及时或者定时发布更新
* 对于有编译过程的代码，比如JAVA，平台提供标准的自动编译脚本程序，省去传war包的人工操作
* 夜间发布更新可以通过平台配置简单的计划任务，自动执行更新，无需人工看守
* 后端代码0秒更新，省去客户端更新的麻烦
* 集成app渠道分发平台，自动提示客户端版本更新消息

##### 3.3 可选组件
* 推送服务JPUSH
* 短信服务[聚合]
* 地理位置服务[高德]
* 支付服务[微信、支付宝]

##### 3.3 数据备份流程
2.x版本迭代功能~

##### 3.4 集成IDE工具插件
3.x版本迭代功能~
