---
title: FAQ
linktitle: 常见问题
type: book
date: "2021-07-03T23:00:00+08:00"

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 9
---

## 一. 修改网站名

- 目的

  ```
  修改网站名称
  ```

- 解决

  修改文件./config/_default/config.yaml

  ```
  title: 'My Project' # Website name
  ```

  

## 二. 顶层导航增加

- 目的

  ```
  新增目录
  ```

![image-20210630233522210.png](https://gitee.com/y0086/documentimage/raw/master/img/image-20210630233522210.png)

- 解决

  - 1.在./content目录下新增ops文件夹和ops文件夹下面_index.md

    ```
    ##ops
    ####_index.md
    ---
    title: 运维
    type: book  # Do not modify.
    toc: false
    ---
    ```

    ![image-20210630233110790](https://gitee.com/y0086/documentimage/raw/master/img/image-20210630233110790.png)

  - 2.修改./config/_default/menu.yaml

    ```yaml
    name: 运维
    #url 为文件夹名称
    url: ops/
    weight: 20
    ```

    

##  三. 网站切换中文

- 目的

  ```
  网站不会显示需要翻译
  ```
  
- 解决

  - 1.修改配置文件./config\_default/languages.yaml

    ```yaml
    # Default language
    en:
      languageCode: en
    修改为
    # Default language
    zh:
      languageCode: zh
    ```

    

  - 2.修改./config\_default/config.yaml

    ```yaml
    ## LANGUAGE
    ############################
    defaultContentLanguage: en
    修改为
    ## LANGUAGE
    ############################
    defaultContentLanguage: zh
    ```

## 四. 编译

- 编译成静态文件

    ```shell
    hugo --baseUrl="/"
    ```

- 编译成docker

    ```shell
    docker build -t guid_web:1.0 .
    ```
## 五. 部署
- 使用docker 启动

    ```shell
    docker run --name my_guid_web -p 80:80 --rm -d guid_web:1.0
    ```
- 使用docker-compose 启动

    ```shell
    cd docker
    docker-compose -f docker-compose.yml up -d
    ```

