title: 如何使ecplise修改java不需要重启
author: JH·D
tags: []
categories: []
date: 2018-04-23 21:21:00
---
##### 如何设置ecplise，修改完代码不重新部署立马生效？
###### 前言：
		由于最近换了工作，新公司项目多而乱，之前用习惯的myecplise有点应付不过来（特别卡，因为它含有各种插件），idea又不太会用，所以无奈之下只能使用了ecplise。但是有一点不爽的是，修改完代码不能立刻生效，要么就是tomcat自动重新部署。导致开发效率严重下降。万事总有解决方法，以下就是我与到的问题。以及解决方案，特此记上一贴。
##### 问题描述：
	

###### 1.项目正常启动
![upload successful](/images/pasted-1.png)
###### 2加入或者修改代码：
![upload successful](/images/pasted-2.png)
###### 3保存 会发现重新部署了，这个项目小还好大了的话部署时间长到不能忍受

![upload successful](\images\pasted-3.png)
###### 4修改ecplise 

![upload successful](\images\pasted-4.png)
发现修改代码不重新部署了但是没有效果，烦躁烦躁。

### 解决方案
##### 1修改tomcat配置 双击服务器 选中modules
	
![upload successful](\images\pasted-5.png)

![upload successful](\images\pasted-6.png)

![upload successful](\images\pasted-7.png)
##### 2修改tomcat,server.xml文件

![upload successful](\images\pasted-8.png)

![upload successful](\images\pasted-10.png)
##### 3改ecplise 配置 

![upload successful](\images\pasted-11.png)

##### 重启项目你会发现修改了java代码（除了新加方法，修改方法头的动作）你会发现会立马生效不需要重新部署，开发效率大大提高，剩余时间可以撩个妹子啥的，美滋滋。
### 注意：以上修改使针对项目的，重新发布项目（remove-add)需要重复以上步骤。