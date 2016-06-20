# sa-sdk-javascript

Sensors Analytics JavaScript SDK  

代码埋点参考 http://www.sensorsdata.cn/manual/js_sdk.html  
可视化埋点参考 https://sensorsdata.cn/manual/vtrack_intro.html  

使用建议： 能用代码埋点就用代码埋点，尽量不要用可视化埋点！具体原因参考上面这个文档。  
如有疑问请联系邮箱 shengyonggen@sensorsdata.cn 比较着急的话可以QQ522370351

# 代码埋点最佳实践
1. 控制台： 在代码埋点时，在控制台会打出 console 。每次 track 都会打出一个对象,里面 event 是你设置的事件名，注意观察数据是否和自己想要的一致！如果没出现，就是埋点失败！同时注意观察控制台的报错，会提示各种错误信息，比如事件名不合法，或者属性值无效等！   
2. 后端验证： 设置 debug_mode：true。这里除了会打 console 外，还会发一次 ajax 请求，在后端会再次验证数据是否合法。  
3. 数据导入辅助工具： 这里会汇总数据的错误。  

# 目录版本说明
使用 SDK 前，请将 /dist/版本号 下的文件都下载到你们自己网站目录下面。  
(稳定版) 表示你在1.x 能直接使用的版本，如果你不确定神策分析系统的版本，请使用第一个稳定版。  
如果你想用最新版，请在使用前在微信群里问下，你们的神策分析系统版本是否支持!!!

##### 1.4.1  (稳定版)
把$os 改成 iPhone OS 和 Android 为了跟安卓iphone兼容

##### 1.4.3  (必须已更新过神策分析系统)
增加sa.quick('autoTrack')方法，可以自动追踪pv，增加是否是首日访问等预置属性，和设置首次来源,首次时间等。  
同时对于属性的验证放宽，如果属性名错误，一样会发到后端。之前是会在前端抛掉。目前这样做可以方便在后端看到错误，方便debug错误原因。

##### 1.4.2  (2016-6-15 注意此次修改要同步更新神策系统，未更新会导致数据丢失!!!)
使用服务器端时间




