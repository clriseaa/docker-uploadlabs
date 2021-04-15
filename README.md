## 0x01 Install

#### 2.1 环境要求

若要自己亲自搭建环境，请按照以下配置环境，方可正常运行每个Pass。

|配置项|配置|描述|
|:---|:---|:---|
|操作系统|Window or Linux|推荐使用Windows，除了Pass-19必须在linux下，其余Pass都可以在Windows上运行|
|PHP版本|推荐5.2.17|其他版本可能会导致部分Pass无法突破|
|PHP组件|php_gd2,php_exif|部分Pass依赖这两个组件|
|中间件|设置Apache以moudel方式连接||

#### 2.2 docker快速搭建

下载upload-labs包

```txt
$ git clone https://github.com/clriseaa/docker-uploadlabs.git
```

创建父级镜像

```txt
$ cd docker-uploadlabs/upload-labs/docker
$ docker build -t upload-labs .
```

创建子级镜像

```txt
$ cd docker-uploadlabs/Pass/Pass-01
$ docker build -t upload-labs/pass01 .
```

创建容器

```
$  docker run -d -p 81:80 upload-labs/pass01:latest
```

#### 2.3 访问upload题目页面

```txt
http://you-ip/Pass/Pass-01
```



