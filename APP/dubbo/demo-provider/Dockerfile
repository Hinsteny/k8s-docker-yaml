# ccr.ccs.tencentyun.com/doctorwork/skywalking-agent:latest是包含jre以及skywalking相关jar包基础容器
FROM openjdk:11
LABEL maintainer="Hinsteny.Hisoka"

# 容器的工作目录统一/app
WORKDIR /app
EXPOSE 20880/tcp

# 复制应用压缩文件(此命令包含解压缩功能)
COPY /Users/h/workspace/project/github/dubbo/dubbo-demo/dubbo-demo-provider/target/*.jar /app

# 容器启动后执行的脚本
ENTRYPOINT ["java", " -Djava.net.preferIPv4Stack=true -verbose:class -jar dubbo-demo-provider-2.6.13-SNAPSHOT.jar"]