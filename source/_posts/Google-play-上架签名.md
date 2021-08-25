---
title: Google play 上架签名
date: 2021-08-25 09:57:20
categories:
    - 互联网
tags:
    - Android
---

### 应用上架谷歌商店报错
`Your Android App Bundle uses an upload certificate with a key that is too weak.`
的解决方案

## 生成上传密钥

https://developer.android.com/studio/publish/app-signing#generate-key

## 下载签名工具
(FairGuard)[https://www.fair-guard.com/index/helpcenter.html?id=387]

设置 config.ini 内的配置信息
```

[signinfo]
keystore-path=C:\Users\j\Desktop\zhengwhizz.jks
alias=key0
password=密码
alias-pwd=密码

```
运行命令
` java -jar FairGuard2.8.7.jar -optype_sign_jar -inputfile app.aab `
对aab包进行签名

参考：https://blog.csdn.net/qq_46702493/article/details/111832145
