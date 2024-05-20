# 使用 Nginx 官方镜像作为基础镜像
FROM docker.io/nginx:latest


# 删除默认的 Nginx 网站配置
RUN rm -rf /usr/share/nginx/html/*

# 构建参数，默认值为空
ARG JAR_FILE

# 将 Maven 构建生成的包复制到 Nginx 默认网站目录下
COPY target/${JAR_FILE} /usr/share/nginx/html/

# 暴露 Nginx 默认端口
EXPOSE 80
