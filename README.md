# uni-app项目模板（不喜勿喷）
> web前端开源的uni-app快速开发模板，参考学习一同进步
> 建议uni-app使用时间达到1年以上的程序员来学习

### 使用步骤
1. 下载下来，解压成文件夹
2. 把项目包丢到HBuilder X里面
3. HBuilder X要安装scss/sass编译插件
4. 运行项目
### 文件说明
1. components/chat-emojis.nvue 表情组件（表情、收藏表情图、表情包）
2. components/chat-message.nvue 消息显示及类型组件
3. components/chat-preview.nvue 图片及视频预览组件
4. components/chat-tabbar.nvue 底部操作组件（语音、输入框、发送）
5. utils/emojis.js 表情数据
6. utils/utils.js 工具
7. chat.nvue 聊天主页面
8. config.js 聊天配置页面及对接页面（所有的聊天对接都提取到这里了）

### 功能
1. 发 文本和表情
2. 发 表情图片
3. 发 图片
4. 发 视频
5. 发 语音
6. 发 位置
7. 发 文件
8. 发 商品
9. 禁言

### 支持聊天类型 
1. 单聊
2. 群聊

### 消息渲染
1. 发送图片、视频、文件先预渲染到页面（有上传进度），模仿微信上传图片
2. 发送消息有发送中、发送失败（可点击重发）、发送成功
3. 已读、未读（有样式、后端没实现）


## 架构功能清单
### 组件示例
1. 瀑布流列表
2. 防抖音滑动视频（带进度加载）
3. 项目主题色介绍
4. 头部导航示例
5. 上拉加载，下拉刷新列表
6. 地区选择
7. 弹窗输入框
8. 滑动操作
9. 富文本编译

### SDK示例
1. 接口请求
2. APP版本更新
3. 支付
4. 分享
5. 小程序登录
6. 公众号登录
7. 登录拦截
8. 获取当前位置
9. 图片上传/文件上传
10. 七牛云图片上传/文件上传
11. 保存图片到相册
12. webSocket封装介绍
13. 公众号SDK
14. APP权限判断和跳转到系统设置
15. 常用工具

### 模板页面
1. 登录
2. 注册
3. 忘记密码
4. 绑定手机号
5. 协议

### 项目结构

``` bash
├── components                              // 组件
│   ├── common                              // 公共组件
│   └── module                              // 项目组件
├── config                                  // 配置						// vuex主文件
│   ├── baseUrl.js                          // 项目配置
│   ├── html5Utils.js                       // H5相关的功能（公众号支付、公众号登录）
│   ├── login.js                            // 小程序登录js代码部分和登录拦截器代码
│   ├── requestConfig.js                    // 接口请求配置
│   ├── socket.js                           // webSocket相关代码
│   └── utils.js                            // 项目相关工具（公众号分享、小程序分享数据处理、支付、获取经纬度、支付分配）
├── pages  									// 项目页面
├── plugins                                 // 公共SDK（基本上不需要改）
│   ├── APPUpdate                          	// APP版本更新
│   ├── request                          	// 接口请求封装
│   ├── share                           	// APP分享
│   ├── md5.js                           	// md5加密
│   ├── permission.js                       // APP权限判断和打开手机系统设置
│   ├── utils.js                       		// 工具（时间转换、APP和小程序获取经纬度代码）
│   └── wxJsSDK.js                       	// 微信公众号SDK去权限获取页面
├── static                                  // 公共文件
│   ├── demo                          		// 本项目相关的图片（可删除）
│   ├── icon                          		// 项目图标
│   ├── mp-h5                          		// H5第三方包（公众号JS-SDK）
│   ├── mp-weixin                          	// 微信小程序第三方包
│   ├── share                          		// 分享SDK的图标
│   └── navBar                              // 导航组件的图标                  
├── store                          		    // vuex商店
│	├── modules							    // vuex分类
│	│	├── common.js					    // vuex通用数据管理
│	│	├── user.js						    // vuex用户数据管理
│   │	└── order.js                        // vuex订单数据管理
│   └── index.js                          	// vuex方法集合
├── style
│   ├── common.scss                         // 公共样式文件
│   ├── input.scss                         	// 公共表单样式
│   ├── mixin.scss                          // 样式配置文件
│   └── table.scss                          // 本项目相关的css（可删除）
├── unpackage                               // 项目编译后的文件
├── App.vue                                 // 项目主界面
├── main.js                                 // 程序入口文件，加载各种公共组件
├── manifest.json                           // uni-app项目类型及环境配置
├── pages.json                           	// 项目路由及项目界面配置
├── README.md                               // 项目介绍文件
└── template.h5.html                        // 项目发布的时候使用的文件
```
