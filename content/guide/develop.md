---
title: Develop
linktitle: 编译
type: book  # Do not modify.
weight: 2
---

#### 一. 目录说明

```shell 
├─assets
│  └─media    [icon.png] 网站图标
│      └─icons
├─config
│  └─_default [config]: 配置和一级菜单(最上那层导航栏)等
├─content     [content]: markdown文件目录，也是编写使用的目录。
│  ├─guide
│  ├─home
│  └─thanos
├─data
│  ├─fonts
│  └─themes
├─uploads 
```

#### 二. 编译

```shell
hugo --baseUrl="/yao/"
baseUrl: /yao/ 访问url为 test.com/yao/
baseUrl: / 访问url为 test.com/
```



{{< cta cta_text="👉 Get Started with ops" cta_link="ops" >}}
