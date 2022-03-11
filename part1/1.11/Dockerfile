FROM openjdk:8-alpine

EXPOSE 8080

WORKDIR /usr/src/app

RUN apk update -y && apk add maven -y
RUN apk update && apk add dos2unix -y

COPY . .

RUN dos2unix mvnw
RUN ./mvnw package

CMD ["java", "-jar", "./target/docker-example-1.1.3.jar"]