FROM openjdk:8-jre-slim
MAINTAINER xuxueli

ENV PARAMS=""

ENV TZ=PRC
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

ADD target/xxl-job-admin-2.3.0.zip /app.zip
RUN unzip -o app.zip \
    && rm -rf app.zip

ENTRYPOINT ["sh","-c","java -jar $JAVA_OPTS /xxl-job-admin-2.3.0/xxl-job-admin-2.3.0.jar $PARAMS"]