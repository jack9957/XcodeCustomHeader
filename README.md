# XcodeCustomHeader
Xcode自定义头部信息

###### 这是Xcode自定义的头部信息 

![自定义](https://github.com/liyang123/XcodeCustomHeader/blob/master/images/Snip20190509_3.png)

我们的目标是

![目标](https://github.com/liyang123/XcodeCustomHeader/blob/master/images/Snip20190509_5.png)

#### 实现步骤

1. 先创建一个命名为**IDETemplateMacros.plist**的文件
2. 以Source Code的方法进行编辑
3. 内容如下

```Objective-C
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
	<key>FILEHEADER</key>
	<string>
//  ___FILENAME___
//  ___PACKAGENAME___
//
//  Author:     lee
//  CSDN:       https://blog.csdn.net/weixin_38554258
//  Email:      coderlee0102@qq.com
//  CreateDate: ___DATE___
//
    </string>
</dict>
</plist>
```

   	4. 保存文件,放在指定目录下. 在不同的目录下,作用的范围不同
       1.  存放在该目录下,对当前 Project 指定的用户（username）有影响  `<ProjectName>.xcodeproj/xcuserdata/[username].xcuserdatad/IDETemplateMacros.plist`
          2.  存放在该目录下,对当前 Project 所有的用户有影响  `<ProjectName>.xcodeproj/xcshareddata/IDETemplateMacros.plist`
          3.  存放在该目录下,对当前 Workspace 所有的用户有影响  `<WorkspaceName>.xcworkspace/xcshareddata/IDETemplateMacros.plist`
          4.  存放在该目录下,对 Xcode 所有创建的文件都有影响 `~/Library/Developer/Xcode/UserData/IDETemplateMacros.plist`

[参考资料](https://help.apple.com/xcode/mac/9.0/index.html#/devc8a500cb9)

[plist模板地址](https://github.com/liyang123/XcodeCustomHeader)

