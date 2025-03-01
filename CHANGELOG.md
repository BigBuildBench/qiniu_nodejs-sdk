## CHANGE LOG

## 7.14.0
- 对象存储，持久化处理支持工作流模版
- 对象存储，修复持久化处理闲时任务的类型声明

## 7.13.0
- 对象存储，新增空间级别上传加速开关
- 对象存储，优化断点续传开启方式
- 对象存储，优化回调签名验证函数，新增兼容 Qiniu 签名
- 对象存储，修复上传失败无法完成自动重试
  - 在 Node.js 18 及以上触发
  - 7.12.0 引入
- 对象存储，新增空间的创建、删除、按标签列举
- 对象存储，调整查询区域主备域名
- 修复内部 HttpClient 部分方法参数类型声明不正确

## 7.12.0
- 对象存储，新增支持 Promise 风格异步
- 对象存储，修复分片上传 v1 在特定条件可能无法从断点继续上传
- 对象存储，新增支持新的区域对象 Region
- 对象存储，管理接口支持双活
- 对象存储，修复缺失的部分类型声明，新增响应的类型声明

## 7.11.1
- 对象存储，上传策略移除严格模式，支持任意策略选项

## 7.11.0
- 对象存储，新增支持归档直读存储
- 对象存储，批量操作、解冻操作支持自动查询 rs 服务域名

## 7.10.1
- 对象存储，修复无法上传带有英文双引号的文件

## 7.10.0
- 对象存储，上传支持双活
- 对象存储，上传回调支持 Promise 风格
- 对象存储，修复分片上传v2在创建 uploadId 失败后仍尝试上传

## 7.9.0
- 对象存储，修复无法对 key 为空字符串的对象进行操作
- 对象存储，查询区域域名支持配置 UC 地址
- 对象存储，查询区域域名接口升级
- 对象存储，更新设置镜像源的域名
- 对象存储，新增请求中间件逻辑，方便拓展请求逻辑
- 对象存储，新增备用 UC 域名用于查询区域域名
- 对象存储，移除首尔区域
- 对象存储，新增 华东浙江2 区域的类型声明

## 7.8.0
- 移除不推荐域名，并增加 亚太-首尔 和 华东-浙江2 固定区域
- RTC，优化请求失败的错误信息
- 对象存储，优化分片上传 ctx 超时检测
- 对象存储，修复事件、跨域部分 API 身份认证错误（v7.7.0 引入）
- 对象存储，新增事件、跨域 API 的类型声明（.d.ts）

## 7.7.0
- 对象存储，管理类 API 发送请求时增加 [X-Qiniu-Date](https://developer.qiniu.com/kodo/3924/common-request-headers) （生成请求的时间） header

## 7.6.1
- 添加sms typing

## 7.6.0
- 对象存储，新增 setObjectLifeCycle 设置对象生命周期 API

## 7.5.0
- 对象存储，新增支持 [深度归档存储类型](https://developer.qiniu.com/kodo/3956/kodo-category#deep_archive)
- 对象存储，修复在不制定区域信息情况下自动获取区域信息异常问题
- 修复 Qiniu 签名算法在对部分 http header 处理异常问题

## 7.4.0
- 支持 [分片上传 V2](https://developer.qiniu.com/kodo/6364/multipartupload-interface)


## 7.3.3
- 修复上传策略中forceSaveKey指定无效

## 7.3.2
- 修复crc32指定值无效
- 修复checkCrc指定无效
- 统一checkCrc类型

## 7.3.1
- 新增归档存储解冻接口
- 支持上传时key值为空字符串

## v7.3.0
- 新增 19 个bucket及文件相关操作
- 新增文件列举 v2 接口功能
- 新增短信功能
- 更新上传加速域名策略
- 修复自动获取上传区域时的无效缓存
- 修复大文件上传异常
- 增加测试用例

## v7.2.2
- 一些log输出问题，travis增加eslint 检查

## v7.2.1
- 修复rtc获取回复存在的问题

## v7.2.0
- 修复node的stream读取的chunk大小比较随意的问题

## v7.1.9
- 修复新版node下resume up方式文件内容被缓存而导致的上传失败

## v7.1.8
- 修复 index.d.ts 文件中zone的设置

## v7.1.7
- 修复form上传在升级mime库后的错误

## v7.1.6
- 修复rs和rsf的https默认域名
- 升级修复mime库的安全风险

## v7.1.5
- 增加连麦功能

## v7.1.3
- 增加新加坡机房

## v7.1.2
- 增加自定义资源访问响应头部的功能
- 改进时间戳签名方法，支持复杂urlencode

### v7.1.1
- 修复 index.d.ts 中的函数声明错误

### v7.1.0
- 修复时间戳防盗链中存在特殊字符引发的签名错误
- 修复分片上传的时候最后一块小于2056字节引发的错误

### v7.0.9
- 增加Qiniu方式的管理凭证生成方法以支持新的产品鉴权

### v7.0.8
- 修复分片上传小文件的时候文件读取end的事件bug

### v7.0.7
- 给form upload添加默认的crc32校验以避免网络层面的字节反转导致上传内容不正确
- 修复resume upload在上传小文件的时候出现的上传失败情况

### v7.0.6
- 修复时间戳防盗链算法中对文件名的urlencode不兼容问题
- 发布index.d.ts文件

### v7.0.5
- 修复zone获取失败时callbackFunc不存在的问题
- 增加分片上传的时候的progressCallback

### v7.0.4
- 增加http&https代理功能

### v7.0.2
- 修复cdn刷新文件和目录中方法引用错误

### v7.0.1

- 重构文件表单上传和分片上传代码
- 重构CDN操作相关的代码
- 重构资源管理相关的代码
- 重构数据处理相关的代码
- 重构上传策略的相关代码

### v6.1.14

2017-01-16

- 增加CDN刷新、预取
- 增加获取带宽、流量数据
- 增加获取日志列表
- 增加时间戳防盗链签名

### v6.1.13

2016-10-13

- 修正从uptoken获取bucket

### v6.1.12

2016-10-10

- 增加多机房接口调用支持

### v6.1.11

2016-05-06

- npm 通过travis 自动发布

### v6.1.10

2016-04-25

- list 增加delimiter 支持
- 增加强制copy/move
- 底层使用putReadable 谢谢 @thesadabc
- 修正result 处理 谢谢 @loulin
- fix Unhandled stream error in pipe 谢谢@loulin
- putExtra 修正 paras 为 params

### v6.1.9

2015-12-03

- Make secure base url
- policy add fsizeMin
- 修正 getEncodedEntryUri(bucket, key)
- 文档修正

### v6.1.8

2015-05-13

- 上传增加putpolicy2

### v6.1.7

2015-05-09

- 上传putpolicy2增加 callbackHost、persistentPipeline, callbackFetchKey
- 增加fetch 函数
- imageview -> imageview2


### v6.1.6

2014-10-31

- 上传putpolicy2增加fsizelimit, insertonly


### v6.1.5

2014-7-23 issue [#111](https://github.com/qiniu/nodejs-sdk/pull/111)

- [#109] 统一user agent
- [#110] 更新put policy

### v6.1.4

2014-7-10 issue [#108](https://github.com/qiniu/nodejs-sdk/pull/108)

- [#107] 调整上传host


### v6.1.3

2014-4-03 issue [#102](https://github.com/qiniu/nodejs-sdk/pull/102)

- [#98] 增加pfop 功能
- [#99] 增加针对七牛callback的检查

### v6.1.2

2014-2-17 issue [#96](https://github.com/qiniu/nodejs-sdk/pull/96)

- Content-Length = 0 时的细节修复


### v6.1.1

2013-12-5 issue [#90](https://github.com/qiniu/nodejs-sdk/pull/90)

- 创建buffer前检测


### v6.1.0

2013-10-08 issues [#81](https://github.com/qiniu/nodejs-sdk/pull/81)

- 使用urllib
- 修复callbackUrl的bug
- 调整bucket的下载域名

### v6.0.0

2013-07-16 issue [#56](https://github.com/qiniu/nodejs-sdk/pull/56)

- 遵循 [sdkspec v6.0.4](https://github.com/qiniu/sdkspec/tree/v6.0.4)
