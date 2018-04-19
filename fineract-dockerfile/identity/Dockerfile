FROM openjdk:8-jre-alpine
VOLUME /tmp
ADD service/build/libs/service-0.1.0-BUILD-SNAPSHOT-boot.jar app.jar
RUN /bin/sh -c 'touch /app.jar'
ENV JAVA_OPTS="-Xmx512m -Xms256m"
EXPOSE 8081
#ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]
ENTRYPOINT exec java $JAVA_OPTS -Djava.security.egd=file:/dev/./urandom -jar /app.jar
