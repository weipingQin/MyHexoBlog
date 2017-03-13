---
title: hexo博客搭建常见问题
---
1.今天碰到了一个问题:hexo博客搭建的时候需要在:后面加一个空格[https://xuanwo.org/2014/08/14/hexo-usual-problem/

2.给文章添加标题:
---
title:XXX
---
设置标题 

注意:别忘记 title: 冒号后面有空格 

3.hexo博客如何插入图片:
使用markdown语法: 
很简单 就是在博客的 source根目录下 mkdir img 建立一个文件夹 然后把截图放进去 你用这个语法 ![](/img/图片的名称.png)
(1) 使用本地路径：在hexo/source目录下新建一个img文件夹，将图片放入该文件夹下，插入图片时链接即为/img/图片名称。 
(2) 使用微博图床，地址http://weibotuchuang.sinaapp.com/，将图片拖入区域中，会生成图片的URL，这就是链接地址。

简单的测试一下: 
![test](/img/test.png)