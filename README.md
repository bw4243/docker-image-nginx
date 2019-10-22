#关于nginx docker官方镜像

- 官方镜像默认静态文件放置路径为`/usr/share/nginx/html`

- 官方镜像默认EXPOSE 80端口

- 官方镜像模型容器启动时的CMD命令为`["nginx", "-g", "daemon off"]`，且没有设置ENTRYPOINT指令

- 官方镜像默认`nginx.conf`位于`/etc/nginx`

- 官方镜像默认`access.log`和`error.log`日志都位于`/var/log/nginx`目录下，同时做了两个软链`ln -sf /dev/stdout /var/log/nginx/access.log`和`ln -sf /dev/stderr /var/log/nginx/error.log`

# 关于本镜像Dockerfile

- 覆盖了`etc/nginx/nginx.conf`、`/etc/nginx/fastcgi.conf`
。