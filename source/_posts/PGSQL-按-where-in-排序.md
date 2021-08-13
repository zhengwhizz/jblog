---
title: PGSQL 按 where in 排序
date: 2021-08-13 03:52:11
tags: PGSQL 数据库
---

## 
`select * from users where id in(18,16,1) order by position(','||id::text||',' in ',18,16,1,')`