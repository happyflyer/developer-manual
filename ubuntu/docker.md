# [Docker](https://www.runoob.com/docker/docker-hello-world.html)

## 1. 容器使用

### 1.1. 创建

```bash
docker run -it image_name:image_tag /bin/bash
```

```bash
docker run -it image_id /bin/bash
```

```bash
docker run -itd --name container_name image_id /bin/bash
```

```bash
docker ps
```

```bash
docker ps -a
```

```bash
docker start container_id
```

```bash
docker stop container_id
```

```bash
docker restart container_id
```

### 1.2. 离开

```bash
# ^ = Ctrl
^p + ^q
```

### 1.3. 进入

```bash
# 不推荐
docker attach container_id
```

```bash
# 推荐
docker exec -it container_id /bin/bash
```

### 1.4. 监视

```bash
docker port container_id
```

```bash
docker logs -f container_id
```

```bash
docker top container_id
```

### 1.5. 删除

```bash
docker rm -f container_id
```

```bash
docker container prune
```

### 1.6. 导出

```bash
docker export container_id > ubuntu.tar
```

### 1.7. 导入

```bash
docker import ubuntu.tar
docker tag image_id image_name:image_tag
```

### 1.8. 提交

```bash
docker commit -m="message" -a="author" container_id docker/ubuntu:v2
```

## 2. 镜像使用

### 2.1. 查看

```bash
docker images
```

```bash
docker search httpd
```

### 2.2. 拉取

```bash
docker pull ubuntu
```

```bash
docker pull ubuntu:16.04
```

### 2.3. 删除

```bash
docker rmi ubuntu:16.04
```

### 2.4. 构建

```bash
docker build -t ubuntu:v2 .
```

### 2.5. 导出

```bash
docker save image_id > ubuntu_v2.tar
```

`save` 和 `export` 的区别：

- `save` 保存镜像所有的信息（包含历史）
- `export` 只导出当前的信息

> 推荐使用 `save`

### 2.6. 导入

```bash
docker load < ubuntu_v2.tar
docker tag image_id ubuntu:v2
```

镜像导入和容器导入的区别：

- 容器导入是将当前容器变成一个新的镜像
- 镜像导入是复制的过程
