---
title: Android动画学习
---

1月的工作中有涉及到动画方面的知识，项目上线了，现在回顾和总结一下涉及到的动画知识和实际解决问题方面的经验。

首先拿到两个小的需求：实现一个Wifi扫描效果动画和一个按钮动画。
效果如下图所示:

首先分析一下这个动画的组成：
动画分两层:外层是一个放大的动画，内层是一个逐帧动画。外部不断的放大然后复原，内部是一个图片的轮换变化，内部的动画还包含一个渐变的过程。
内部的逐帧动画是由若干张图片构成，可以采用SVG的方式来进行加载，放到一个xml文件中去实现 

``` 
<?xml version="1.0" encoding="utf-8"?>
<animation-list xmlns:android="http://schemas.android.com/apk/res/android"
    android:oneshot="false">

    <item
        android:drawable="@drawable/wifi_1"
        android:duration="400" />
    <item
        android:drawable="@drawable/wifi_2"
        android:fromAlpha = "0.2"
        android:toAlpha = "0.0"
        android:duration="400" />
    <item
        android:drawable="@drawable/wifi_3"
        android:fromAlpha = "0.2"
        android:toAlpha = "0.0"
        android:duration="400" />

    <item
        android:drawable="@drawable/wifi_4"
        android:fromAlpha = "0.2"
        android:toAlpha = "0.0"
        android:duration="400" />

</animation-list>
```