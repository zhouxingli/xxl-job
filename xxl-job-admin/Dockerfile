FROM 192.168.100.118:5000/library/openjdk:8-jdk-alpine_font

RUN mkdir -p /model/graphql

WORKDIR /model/graphql

EXPOSE 8300

ADD ./target/reportcenter-service.jar ./app.jar

ENTRYPOINT ["java", "-Djava.security.egd=file:/dev/./urandom", "-jar", "app.jar"]

CMD ["--spring.profiles.active=dev"]
