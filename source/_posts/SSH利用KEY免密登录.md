---
title: SSH利用KEY免密登录
date: 2021-08-25 21:16:20
categories:
    - 互联网
tags:
    - SSH
    - Ubuntu
    - VSC
 
---

## A 机登录 B 机


在 A 机使用 ` ssh-keygen ` 生成秘钥，复制 `id_rsa.pub` 文件中的公钥，

在 B 机 ` echo '你的公钥' >> ~/.ssh/authorized_keys ` 把公钥保存好。
更改文件权限 ` chmod 600 ~/.ssh/authorized_keys ` 之后就可以从 A 机免密登录 B 机了。

### 同样适用于 VSC 远程连接。


