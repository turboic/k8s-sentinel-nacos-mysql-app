FROM java:8
MAINTAINER demo@test.io
ENV MYPATH /
WORKDIR $MYPATH
ARG JAR_FILE=sentinel-dashboard.jar
COPY ${JAR_FILE} sentinel-dashboard.jar
RUN ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime
RUN echo 'Asia/Shanghai' >/etc/timezone
EXPOSE 8080
EXPOSE 8719
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","sentinel-dashboard.jar"]