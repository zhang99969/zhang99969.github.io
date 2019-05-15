## iOS中使用Stream

#### 1. 下载和安装

###### (1) 下载Stream
###### (2) 同意使用vpn
###### (3) 跳转到浏览器下载证书
###### (4) 打开设置-通用-描述文件，安转下载好的 Stream Generated CA 描述文件
###### (5) 打开设置-通用-关于本机-证书信任设置 开启针对根证书启动完全信任

#### 2. 开始抓包

#### 3. 抓包处理

###### (1) 点击抓包历史，进入历史记录。可以通过右上角放大镜图标筛选文件，如JSON类型。
###### (2) 点击某JSON文件，点击上侧相应，在相应主体中选择查看相应，得到JSON文件的具体内容。可点击右上角分享按钮进行拷贝。

------


> 出自：[Edward_is_1ncredible _Blog](https://blog.csdn.net/Edward_is_1ncredible/article/details/84023572)
> 欣赏。
> Origin From [Edward_is_1ncredible _Blog](https://blog.csdn.net/Edward_is_1ncredible/article/details/84023572))
> Special Appreciate.

## [Python爬虫] 7-Charles抓取微信小程序
最近在尝试抓取微信的小程序，用到了Charles，微信小程序的话需要使用HTTPS抓包，网上有些教程内容有步骤的缺失，所以重新整理一份傻瓜式的教程，环境WIN10+IOS，内容基于Roy_Liang前辈：https://www.jianshu.com/p/5539599c7a25：

#### 1. Charles安装
官网下载安装Charles:https://www.charlesproxy.com/download/

#### 2. HTTPS抓包准备工作
###### 1)关闭防火墙
###### 2)查看电脑的IP地址：cmd->ipconfig
![img](https://img-blog.csdnimg.cn/20181113093732652.png)

###### 3)设置手机HTTP代理：设置->无线局域网->连接的WiF

####### **1.前提是将手机和电脑连入同一个WIFI**
####### **2.设置代理后，需要在电脑上打开Charles才能上网**

电脑IP地址：如192.168.3.4，端口：8888
![img](https://img-blog.csdnimg.cn/2018111309414933.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Vkd2FyZF9pc18xbmNyZWRpYmxl,size_16,color_FFFFFF,t_70)

###### 4)手机端证书的安装

Charles：Help -> SSL Proxying -> Install Charles Root Certificate on a Mobile Device
![img](https://img-blog.csdnimg.cn/20181113094856356.png)

根据提示到：chls.pro/ssl 这个地址进行下载安装，安装完毕后
手机端：设置->通用->描述文件与设备管理，要开启下载的证书

![img](https://img-blog.csdnimg.cn/20181113095150643.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Vkd2FyZF9pc18xbmNyZWRpYmxl,size_16,color_FFFFFF,t_70)

###### 5)PC端证书的安装
Charles：Help -> SSL Proxying -> Install Charles Root Certificate，默认安装，安装完毕后
Charles：Proxy->SSL Proxying-> Add ：Host：*，Port：443

![img](https://img-blog.csdnimg.cn/20181113095749905.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Vkd2FyZF9pc18xbmNyZWRpYmxl,size_16,color_FFFFFF,t_70)

#### 3. HTTPS抓包
首先这个去掉之后可以只抓取移动端的内容
![img](https://img-blog.csdnimg.cn/20181113094527631.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Vkd2FyZF9pc18xbmNyZWRpYmxl,size_16,color_FFFFFF,t_70)

可以正常获取内容了：
![img](https://img-blog.csdnimg.cn/20181113100145124.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Vkd2FyZF9pc18xbmNyZWRpYmxl,size_16,color_FFFFFF,t_70)

> 点击[Edward_is_1ncredible _Blog](https://blog.csdn.net/Edward_is_1ncredible/article/details/84023572)留下你的评论
> 欣赏。
> Your text at [Edward_is_1ncredible _Blog](https://blog.csdn.net/Edward_is_1ncredible/article/details/84023572)
> Special Appreciate.

------

> 出自：[Roy_Liang_Blog](https://www.jianshu.com/p/5539599c7a25)
> 欣赏。
> Origin From [Roy_Liang_Blog](https://www.jianshu.com/p/5539599c7a25)
> Special Appreciate.

## 十分钟学会Charles抓包(iOS的http/https请求)

- Charles安装
- HTTP抓包
- HTTPS抓包

#### 1. Charles安装

官网下载安装Charles:
 [https://www.charlesproxy.com/download/](https://link.jianshu.com?t=https://www.charlesproxy.com/download/)

#### 2. HTTP抓包

###### （1）查看电脑IP地址
![img](https:////upload-images.jianshu.io/upload_images/2469183-ff851ce2abe6cfe8.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/672/format/webp)
###### （2）设置手机HTTP代理
手机连上电脑，点击“设置->无线局域网->连接的WiFi”，设置HTTP代理：
 服务器为电脑IP地址：如192.168.1.169
 端口：8888
![img](https:////upload-images.jianshu.io/upload_images/2469183-ad19fa10a1815cbc.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/350/format/webp)
设置代理后，需要在电脑上打开Charles才能上网
###### （3）电脑上打开Charles进行HTTP抓包
手机上打开某个App或者浏览器什么的，如果不能上网，检查前面步骤是否正确
![img](https:////upload-images.jianshu.io/upload_images/2469183-8630cf0087d20187.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/782/format/webp)
点击“Allow”允许，出现手机的HTTP请求列表
![img](https:////upload-images.jianshu.io/upload_images/2469183-874a256420dcae1f.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1000/format/webp)
HTTP抓包
#### 3. HTTPS抓包
HTTPS的抓包需要在HTTP抓包基础上再进行设置
设置前抓包HTTPS是这样的
![img](https:////upload-images.jianshu.io/upload_images/2469183-81c9d7cd686f86eb.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/636/format/webp)
设置后抓包HTTPS长这样
![img](https:////upload-images.jianshu.io/upload_images/2469183-3b9210f6ea4c6403.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/626/format/webp)
![img](https:////upload-images.jianshu.io/upload_images/2469183-c83e45626a1cb35e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1000/format/webp)
> **以下为在HTTP抓包基础上进行HTTP抓包的进一步设置步骤:**

###### （1）安装SSL证书到手机设备

点击 Help -> SSL Proxying -> Install Charles Root Certificate on a Mobile Device
![img](https:////upload-images.jianshu.io/upload_images/2469183-8f47a1b1c1540ef7.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1000/format/webp)
出现弹窗得到地址 [chls.pro/ssl](https://link.jianshu.com?t=chls.pro/ssl)
![img](https:////upload-images.jianshu.io/upload_images/2469183-c7f6ad4a204b0bd4.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/699/format/webp)

手机安装SSL证书的地址
在手机Safari浏览器输入地址 [chls.pro/ssl](https://link.jianshu.com?t=chls.pro/ssl)，出现证书安装页面，点击安装
 手机设置有密码的输入密码进行安装
![img](https:////upload-images.jianshu.io/upload_images/2469183-7ed4a5c8c2a36217.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/249/format/webp)

安装证书

-  *注意1：*有兄弟姐妹说Safari浏览器输入这个网址[chls.pro/ssl](https://link.jianshu.com?t=chls.pro/ssl)安装不了证书的情况,
   亲测要(1)设置好手机HTTP代理    (2)电脑上Charles要开着
-  *注意2：*iOS 10.3系统，需要在 *设置→通用→关于本机→证书信任设置* 里面启用完全信任Charles证书
   （这里感谢[@13002171223](https://www.jianshu.com/users/d4b6b76e81da)的提出这点 ，之前没升级10.3哈）

###### （2）Charles设置Proxy

Proxy -> SSL Proxying Settings...
![img](https:////upload-images.jianshu.io/upload_images/2469183-2c460b4652797ccf.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/549/format/webp)

勾选Enable SSL Proxying,点击Add
![img](https:////upload-images.jianshu.io/upload_images/2469183-11eb2be75eae13fb.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/592/format/webp)

Host设置要抓取的https接口，比如想抓这个
![img](https:////upload-images.jianshu.io/upload_images/2469183-b39831342a11daca.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/285/format/webp)

 Host填写：https://api.weibo.cn
 Port填写：443
![img](https:////upload-images.jianshu.io/upload_images/2469183-ca37de9cdb920511.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1000/format/webp)

###### （3）进行HTTPS抓包
让手机重新发送https请求，可看到抓包
![img](https:////upload-images.jianshu.io/upload_images/2469183-5f1b21912781d466.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1000/format/webp)

HTTPS抓包
注意：不抓包请关闭手机HTTP代理，否则断开与电脑连接后会连不上网

> 点击[Roy_Liang_Blog](https://www.jianshu.com/p/5539599c7a25)留下你的评论
> 欣赏。
> Your text at [Roy_Liang_Blog](https://www.jianshu.com/p/5539599c7a25)
> Special Appreciate.
