# docker-nginx
 在Ubuntu虚拟机环境，基于Docker部署Nginx Web服务，使用alpine精简镜像。

## 项目环境
- 宿主机：VMware虚拟机 Ubuntu 24.04
- Docker版本：29.1.3
- 镜像：nginx:alpine（轻量精简镜像）

## 功能说明
1. 基于Dockerfile自定义构建Nginx镜像，替换默认首页
2. 端口映射，外部可访问Web服务
3. 使用容器数据卷，实现配置文件与容器解耦
4. 配置Docker国内镜像加速器，提升镜像拉取效率

## 快速部署
```bash
# 构建镜像
docker build -t my-nginx .
# 启动容器
docker run -d -p 8080:80 --name nginx-demo my-nginx
# 访问：虚拟机IP:8080
