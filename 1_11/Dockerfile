FROM amazoncorretto:8-alpine

EXPOSE 8080

WORKDIR /app

COPY . .

RUN chmod +x mvnw

RUN ./mvnw package

CMD ["java", "-jar", "./target/docker-example-1.1.3.jar"]