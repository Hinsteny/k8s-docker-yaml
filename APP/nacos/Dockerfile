# ccr.ccs.tencentyun.com/doctorwork/skywalking-agent:latest是包含jre以及skywalking相关jar包基础容器
FROM openjdk:11
LABEL maintainer="Hinsteny.Hisoka"

# 容器的工作目录统一/app
WORKDIR /app
EXPOSE 20880/tcp

# 复制nacos的执行文件
ADD target/nacos-server-1.0.0-RC3/nacos/ /app/

# 容器启动后执行的脚本
ENTRYPOINT ["sh", "/app/bin/startup.sh", "-m standalone"]