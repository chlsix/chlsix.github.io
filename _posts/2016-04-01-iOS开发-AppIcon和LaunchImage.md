---
title: iOS开发-AppIcon和LaunchImage
categories: 
- iOS
tags: iOS开发
---

# 引言  
对于一款App，图标和启动图是必不可少。好看的图标和启动图会更加地吸引用户，能增加点击量和下载量，为你的App大大的加分。而且启动图设置是有尺寸要求的，系统会根据启动图，辨别适配的是哪个机型。

# 设置AppIcon

## 1. AppIcon尺寸
AppIcon有多种尺寸，下面仅列出iPhone上常用的尺寸，ipad等其他设备的尺寸，请自行查看[官方文档](https://developer.apple.com/library/ios/qa/qa1686/_index.html)


![iPhone图标尺寸](http://upload-images.jianshu.io/upload_images/679533-a4c0d3efc0d28768.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

## 2. 添加AppIcon

在General中启用AppIcon

![启用AppIcon.gif](http://upload-images.jianshu.io/upload_images/679533-a5f6155208022326.gif?imageMogr2/auto-orient/strip)

右边栏中可以选择要添加的类型，一般选择iPhone一项中的iOS7.0andLater即可

![可选的类型.png](http://upload-images.jianshu.io/upload_images/679533-9416dcfe2802762d.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

把图片拖入相应位置，这样就设置好了AppIcon，重新编译运行就能看到图标了。

![拖入图片之前.png](http://upload-images.jianshu.io/upload_images/679533-ff6cefe1daf1ff56.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


![拖入图片之后.png](http://upload-images.jianshu.io/upload_images/679533-5237df39abd8c4cd.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

**小技巧**：一般图标都是让美工提供，如果美工比较忙的的话，可以只提供一张1024*1024的图片，我们可以自己生成。生成地址:[图标工场](http://icon.wuruihong.com/)

生成之后下载，会到的所需要的所有尺寸

![文件夹内容.png](http://upload-images.jianshu.io/upload_images/679533-c972e74a7eb4236c.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

可以直接将AppIcon.appiconset文件夹直接导入Assets.xcassets中使用，但由于很多尺寸用不上，建议还是导入必须的图片就可以了。

# 设置LaunchImage

## 1. LaunchImage尺寸

常用尺寸

iPhone 6Plus/6SPlus(Retina HD 5.5 @3x): 1242 x 2208 
iPhone 6/6S/(Retina HD 4.7 @2x): 750 x 1334
iPhone 5/5S(Retina 4 @2x): 640 x 1136
iPhone 4/4S(@2x): 640 x 960

## 2. 添加LaunchImage

在Assets.xcassets中添加LaunchImage

![添加LaunchImage.gif](http://upload-images.jianshu.io/upload_images/679533-33c8c9bc997a845c.gif?imageMogr2/auto-orient/strip)

同样在右边栏可以选择要添加的类型

![可选类型.png](http://upload-images.jianshu.io/upload_images/679533-53d285a1475fe1c1.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

把图片拖入相应位置

![拖入前.png](http://upload-images.jianshu.io/upload_images/679533-0eb2d4d8e1896319.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![拖入后.png](http://upload-images.jianshu.io/upload_images/679533-adc1d4021a4672e6.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

启用LaunchImage

![启用LaunchImage.gif](http://upload-images.jianshu.io/upload_images/679533-3b609c05b91bc305.gif?imageMogr2/auto-orient/strip)

禁止使用LaunchScreen.storyboard，如果不禁止即使设置了LaunchImage也不会有效果，加载的还是空白的LaunchScreen.storyboard

![禁用LaunchScreen.gif](http://upload-images.jianshu.io/upload_images/679533-dde37fd00d324f8c.gif?imageMogr2/auto-orient/strip)

重新编译运行就能看到启动图画面了。

更多内容请查看[官方文档](https://developer.apple.com/library/ios/recipes/xcode_help-image_catalog-1.0/chapters/Recipe.html#//apple_ref/doc/uid/TP40013303-CH1-SW1)