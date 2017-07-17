---
layout: post
title: "Xcode App AppIcon and LaunchImage"
date:  6/06/17 7:55 PM
tags: 
	-  开发
	-  ios
	-  xcode
---
# 如何在xcode里设置图标和启动图片
## 制作不同尺寸的图标
当我们设计好图标后，可以用这个网站来生成需要的不同尺寸的图标。https://appiconizer.com/
## 制作不同尺寸的启动图片
其对应的size标准可参考下图：[](images/xcode-icons6.png)
{% blockquote @ https://stackoverflow.com/questions/16832459/ios-launch-image-sizes %}
图片参考来源. https://stackoverflow.com/questions/16832459/ios-launch-image-sizes
{% endblockquote %}

## 设置图标
1. 打开Xcode，打开项目，选择项目名-targets，然后打开General->App Icons and Launch Images->App Icons Source，
设置为AppIcon，如下图所示![](images/xcode-icons1.png) 
2.然后点击旁边的箭头，打开图标设置页面。如下图所示![](images/xcode-icons2.png) 
3.其对应的size标准可参考下图：![](images/xcode-icons3.png) 

{% blockquote @developer apple https://developer.apple.com/library/content/qa/qa1686/_index.html %}
图片参考来源. https://developer.apple.com/library/content/qa/qa1686/_index.html
{% endblockquote %}

4.参考上图，下面根据需要把对应大小的图片直接拖到xcode的图标设置页面对应的虚线框内即可。

## 设置启动图片

1.回到General->App Icons and Launch Images->Launch Images Source,点击后出现下图，直接点击Migrate即可。
如下图所示![](images/xcode-icons4.png) 
注意：确保Launch Screen File  这里设为空。如下图所示：
![](images/xcode-icons8.png) 
2.然后点击AppIcon，点击AppIcon下面的LaunchImage，入下图所示：![](images/xcode-icons5.png) 
3.在右侧勾选需要的图片大小，入下图所示：![](images/xcode-icons7.png) 
3.参考图[](images/xcode-icons6.png)，把对应大小的启动图片分别拖到对应的虚线框即可。
 ## 最后就可以点击build来看看最后的效果啦。
