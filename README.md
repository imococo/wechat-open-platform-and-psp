## LICENSE：Apache License


> [License详情](/v1.0/license/index.md)
> 
> [点击查看 Apache License ](https://gitee.com/iYUN2/wechat-open-platform-and-psp/blob/master/LICENSE)
>
> <font color="red">使用声明：你可以使用本框架开发你自己的微信开放平台服务第三方平台、微信支付服务商管理系统以及在此基础上研发的产品，本公司不参与收益分享，严禁在使用本框架的基础上发布与与我公司争夺市场或用户的产品。
> 
> 严禁使用本产品违反中华人民共和国法律从事任何违法犯罪活动，否则后果自负。</font>


<!-- 开发者可以不需要关注授权、ComponentVerifyTicket、ComponentAcceessToken、AuthorizerAccessToken、消息和支付场景下的消息加密、解密即可快速部署你自己的微信开放平台应用。

- [官方网站www.yun2.net ](https://www.yun2.net)

- [了解什么是`uniCloud` 点这里](https://unicloud.dcloud.net.cn/)

如果你在使用中遇到问题、阅读本文档过程中有不理解的地方或发现错误，请加QQ群（<font color="red">416781416</font>）获取支持、提交错误。 -->

## 适合谁用

- 想交流研究 `uniCloud` 技术；
- 想交流研究“微信开放平台”第三方平台+“微信支付服务商”；
- 使用“微信开放平台”第三方平台+“微信支付服务商”应用开发对外提供服务的个人或团队。
- 使用“微信开放平台”第三方平台+“微信支付服务商”为自己（所服务）的企业开发自己的应用。


## 框架特征

使用本框架可以免开发在`uniCloud `面开发快速部署你自己的“微信开放平台”第三方平台+“微信支付服务商”管理系统，可以在本框架基础上进行二次开发。

如果你现有的业务或代码使用其它语言譬如Java，PHP，Go，C#, GO等语言开发不适合移植到`uniCloud腾讯云`的话，可以部署本系统作为中控服务（[了解什么是中控服务](/v1.0/ext/center-controller-service.md)）。

- 基于[微信开放平台第三方平台，详情](https://open.weixin.qq.com)
- 基于[微信支付服务商V3版，详情](https://open.weixin.qq.com)
- 基于[`serverless`，详情](https://uniapp.dcloud.net.cn/uniCloud/#%E4%BB%80%E4%B9%88%E6%98%AFserverless)
- 基于[`uniCloud+腾讯云`，详情](https://uniapp.dcloud.net.cn/uniCloud/)
- 基于[`uni-admin`，详情](https://uniapp.dcloud.net.cn/uniCloud/admin.html)
- 基于[`uni-cloud-router`，详情](https://uniapp.dcloud.net.cn/uniCloud/uni-cloud-router.html)
- 基于[`uni-id`用户体系，详情](https://uniapp.dcloud.net.cn/uniCloud/uni-id-summary.html)


## 使用本框你需要具备的知识
  

- 域名基础知识：注册、实名认证、备案、解析、SSL证书
- 熟悉HTML、CSS、Javascript及ES6的特征：Promise/async/await等、面向对象编程（class/继承）等
- Vue开发经验 [https://cn.vuejs.org/](https://cn.vuejs.org/)： vuex/页面/组件/mixin/route等
- 了解Node、NPM,、Webpack等相关知识
- 了解[微信开放平台](https://open.weixin.qq.com)和[微信支付服务商](https://pay.weixin.qq.com)
- 了解数据库相关知识：数据类型、表设计、索引等
- 了解Redis [https://www.redis.net.cn/](https://www.redis.net.cn/)
- 具有前后端开发经验，具有了解一款后端MVC框架，了解面向对象编程更佳。
  - 前后端交互经验，http/socket，xhr，cookie，referer、跨域等
  - json、xml
  - jwt、token、session、cookie、local storage
- 了解[`uniCloud`服务空间](https://uniapp.dcloud.io/uniCloud/concepts/space.html)及注册
    - [数据库](https://uniapp.dcloud.io/uniCloud/concepts/database.html)
    - [云函数](https://uniapp.dcloud.io/uniCloud/concepts/cloudfunction.html)
    - [云对象](https://uniapp.dcloud.net.cn/uniCloud/cloud-obj.html)
    - [云存储](https://uniapp.dcloud.io/uniCloud/storage.html)
    - [Redis](https://uniapp.dcloud.net.cn/uniCloud/redis-introduction.html)
    - [前端网页托管](https://uniapp.dcloud.net.cn/uniCloud/hosting.html)
- 会使用`HBuilderX`进行`uniapp`类型项目的开发和部署[https://www.dcloud.io/hbuilderx.html](https://www.dcloud.io/hbuilderx.html)

如果不具备以上所需基础知识，在使用本项目或阅读文档时会遇到障碍（虽然我们做了详细的指引），你也可以选择我们的公开课、私教课来补齐这方面的知识，详情联系微信：yun2dialy

    
## 主要功能

> 可以同时管理多个开放平台的第三方平台的授权等；商户实名认证（选择费率）提交后，后台审核通过递交微信支付给商户开户，商户签约成功后，自助生成付款码；一整套类【收Qian吧】的微信收银体系。
> 
> <font color="red">以下打勾表示已完成</font>

- [x] 创建管理多个开放平台，支持生成开放平台第三方平台配置和指引
- [x] 全自动接收维护ComponentVerifyTicket和ComponentAcceessToken更新[详情](#创建微信开放平台)
- [x] 扫码或授权微信公众号/小程序给开放平台，自动管理AuthorizerAccessToken，替代非授权模式下的AccessToken，自动处理授权(添加、更新、取消)事件，拉取授权公众号/小程序信息，支持AccessToken中转服务，[详情](#微信access_token中转服务)
- [x] 已经授权的微信公众号用户关注、取关等都会记录、多维度(年月周日时分秒)统计和图表展示
- [x] 已经授权的微信公众号菜单点击、扫码事件、给公众号发消息都会进行记录
- [x] 授权的公众号如果授权了账号服务，支持生成带参数二维码，并对扫码进行记录、多维度(年月周日时分秒)统计和图表展示
- [x] 媒体资源管理：所有上传的图片，视频，音频，文件资源管理，支持：
	- [x] uniCloud跨空间云存储、
	- [x] 授权服务器号作为云存储使用（永久素材：图片10M内10万张，视频10M内1000个，音频2M1000个）。
- [x] 开放平台快速注册小程序
    - [x] 免300元无限快速注册小程序和管理
    - [ ] 小程序管理
    - [ ] 快速注册小程序代码模版、发布管理
- [x] 商品库管理（添加、编辑、删除商品）
- [ ] 微商城管理（从商品库挑选商品指定价格和库存数上架到商城）
    - [ ] 商城快速注册、认证
    - [ ] 下单后打印小票
    - [ ] 发货后通知
    - [ ] 商品分账等
- [x] 支付
    - [x] 采用[`uniPay`](#https://uniapp.dcloud.net.cn/uniCloud/unipay.html#%E7%AE%80%E4%BB%8B)
    - [x] 使用[YUN2-wxpay-v3](/)微信支付服务商V3版本，已集成下单，支付，库存管理，订单通知，小票打印，统计等逻辑
    - [x] 服务端扩展了商家扫用户付款码逻辑（用户手机无网络状态下支付），有开发能力的可以对接扫描枪硬件收银或联系“YUN2云图”官方定制。
    - [x] 支持支付订单管理、服务商退款（需要特约商户授权服务商户“API退款”） 
    - [ ] 扫脸支付
- [x] 支付服务商
    - [x] 微信支付
    - [ ] 支付宝支付
    - [x] 微信点金服务计划
    - [x] 生成收款码，多维度(年月周日时分秒)统计和图表展示
	- [x] 手机网页收银台（收款码页面，或者收银台页面链接在公众号）
    - [ ] 小程序收银台，含源码
    - [x] 商户管理，服务商进件管理
    - [x] 收银、商品、门店多维度(年月周日时分秒)统计和图表展示
- [x] 登录扩展，需使用一个授权的服务号，用户登录后自动自动创建`uni-id-users`
    - [x] PC端口采用绑定服务号带参数二维码，自定义扫码后推送内容，扫码后自动关注服务号；
    - [x] 微信端则支持“静默snsapi_base”和“授权snsapi_userinfo”两种模式自助切换。
- [x] 小票打印机管理 [https://ext.dcloud.net.cn/plugin?id=9184](https://ext.dcloud.net.cn/plugin?id=9184)
    - [x] 当前支持厂家：佳博、飞鹅、优声云
    - [x] 添加设备（添加到uniCloud，同时添加到厂商云平台）
    - [x] 设置/取消LOGO（部分厂家不支持）
    - [x] 获取打印机设备状态（在线/离线）
    - [x] 打印（仅支持自定义模版打印，不支持16进制模式打印）
    - [x] 异步添加/批量添加打印任务
    - [x] 打印任务浏览，重新打印
    - [x] 异步处理打印任务
- [x] 通知管理
    - [x] 系统运行中的重要日志，警告推送
    - [x] 支持企业微信、短信、邮件等通知方式


## 界面截图

<img style="border:1px solid #aaa;margin-bottom:20px" src="https://dist.yun2.net/documents/screenshot.1.png" width="90%" />

<img style="border:1px solid #aaa;margin-bottom:20px" src="https://dist.yun2.net/documents/screenshot.2.png" width="90%" />

<img style="border:1px solid #aaa;margin-bottom:20px" src="https://dist.yun2.net/documents/screenshot.3.png" width="90%" />

<img style="border:1px solid #aaa;margin-bottom:20px" src="https://dist.yun2.net/documents/screenshot.4.png" width="90%" />


## 部署环境要求

> ### <font color="red">注意：本框架必须搭配`uniCloud腾讯云`+云函数配置`nodejs12`使用</font>


主要原因是目前只有`uniCloud腾讯云`云函数支持`nodejs12`的`keepRunningAfterReturn`，即“`return`后继续执行代码的意思”，场景如下：
  - 公众号开发与服务器交互需要在 5 秒内返回结果给微信服务器，实际开发中有时候在服务端需要处理的数据和运算比较耗时导致出现“该公众号提供的服务出现故障”的错误提示，
而使用`keepRunningAfterReturn`可以返回数据给微信服务器后，继续执行比较耗时的操作譬如生成图片海报，发送客服消息等；

  - 支付场景下支付平台在用户支付后回调到URL化云函数/云对象，使用`keepRunningAfterReturn`可以借助这个回调改变订单支付状态后立刻`return`结果给支付平台，再执行后续操作诸如：
  订单库存扣除、用户支付通知、小票打印、收银统计、分账等一连串耗时操作。
    
目前只有腾讯云的 `nodejs12` 支持 `keepRunningAfterReturn` ，故本框架部署必须搭配`uniCloud腾讯云`+云函数配置`nodejs12`来使用。

> ### [点击了解什么是 `keepRunningAfterReturn`](https://uniapp.dcloud.net.cn/uniCloud/cf-functions.html#keep-running)

> ### [本框架对`keepRunningAfterReturn` 做了封装，详情查看](/v1.0/ext/keepRunningAfterReturn)

## 开发者交流群


<div style="display:inline-flex">
<a target="_blank" href="https://qm.qq.com/cgi-bin/qm/qr?k=qQt7gYylnHRQRf0LXlYyM2rKlboe16Ru&jump_from=webapi"><img border="0" src="//pub.idqqimg.com/wpa/images/group.png" alt="点击加QQ群" title="点击加QQ群"></a>
（群号：416781416）
</div>
