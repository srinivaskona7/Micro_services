FROM maven:3.8.2-openjdk-8-slim as build
WORKDIR /app
COPY . .
RUN mvn install
EXPOSE 1001

#jdk
FROM openjdk:11.0.10-jre-slim
WORKDIR /app
COPY --from=build /app/target/offers-0.0.1-SNAPSHOT.jar /app 

CMD ["java", "-jar", "offers-0.0.1-SNAPSHOT.jar"] 