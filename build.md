### 编译成静态文件

```shell
hugo --baseUrl="/"
```

### 编译成docker

```shell
docker build -t guid_web:1.0 .
```

### 使用docker-compose 启动

```shell
docker run --name my_guid_web -p 80:80 --rm -d guid_web:1.0
```



