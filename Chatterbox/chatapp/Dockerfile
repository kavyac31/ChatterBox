FROM maven:3.8.5-openjdk-17 AS build
COPY . .

FROM openjdk:17.0.1-jdk-slim
COPY --from=build Chatterbox/chatapp/target/chatapp-0.0.1-SNAPSHOT.jar chatapp.jar
EXPOSE 7070
ENTRYPOINT ["java","-jar","chatapp.jar"]
