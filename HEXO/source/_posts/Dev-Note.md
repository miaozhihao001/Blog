---
layout: post
title: Dev-Note
---

开发过程中的小问题记录

<!--more-->

## Dev

1、NSKeyedArchiver 自定义对象写文件
```
如果存储的对象类名有变动，则需要设置clasName, 【setClassName:forClass:】。        
使用 NSKeyedArchiver 进行数据持久化时, 系统会默认使用类名去建表，如果类名变了，那么使用新的类名肯定是从本地获取不到表的。     
所以需要在 NSKeyedArchiver 或者 NSKeyedUnarchiver 时使用 【setClassName:forClass:】 指定类名。    
```

## Debug

1、断点配置：【Generate Debug Symbols】     
```
描述: 用来控制断点是否生效,关闭此功能，打包.ipa时，包体积会小很多。    
path:【project/TARGETS/Build Settings/Apple LLVM7.1 - Code Genneration/Generate Debug Symbols】    
```

2、捕获全局异常：【All Exception】    
```
描述: 用来捕捉整个项目在Xcode里执行时的异常。例如：try/catch时,catch住的异常,【All Exception】可以直接定位到具体位置。     
path: 异常捕捉(commod+7)/Xcode左下角点击+/Add Exception Breakpoint/完成(回车键)  
```


