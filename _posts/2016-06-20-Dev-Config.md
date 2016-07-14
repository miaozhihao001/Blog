---
layout: post
title: Dev-Config
date: 2016-06-20
tag: Dev   
---

一些常用的配置

<!--more-->

## Mac配置    
1、生成SSHKey过程      

```
1.查看是否已经有了ssh密钥：`cd ~/.ssh` ，如果没有密钥则不会有此文件夹，有则备份删除。    
2.生存密钥：ssh-keygen -t rsa -C “test@gmail.com”。   按3个回车，密码为空。       

Your identification has been saved in /home/tekkub/.ssh/id_rsa.
Your public key has been saved in /home/tekkub/.ssh/id_rsa.pub.
The key fingerprint is:
………………    
最后得到了两个文件：id_rsa和id_rsa.pub          
```


## 项目版本控制配置  
1、Mac `versions` 添加.a库   
```  
Xcode自带的svn和Versions以及一些其它工具都不能上传".a"文件。

- 打开终端，输入cd，空格，然后将需要上传的.a文件所在的文件夹（不是.a文件）拖拽到终端（此办法无需输入繁琐的路径，快捷方便） 回车
- 之后再输入如下命令：svn add libGoogleAnalytics.a，回车；
- 之后会出现：A  (bin)  libGoogleAnalytics.a

表示添加成功，打开Versions就可以看到，刚才添加的.a文件，此时就可以手动上传了。
另外，请注意路径的正确性。
```






