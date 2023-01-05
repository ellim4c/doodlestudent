FROM maven:3-jdk-11 as builder
WORKDIR /app
COPY . .
RUN mvn clean package -Dquarkus.package.type=uber-jar

FROM alpine:latest
RUN apk add openjdk11-jre
COPY --from=builder /app/target/tlcdemoApp-1.0.0-SNAPSHOT-runner.jar /app/target/tlcdemoApp-1.0.0-SNAPSHOT-runner.jar
CMD java -jar /app/target/tlcdemoApp-1.0.0-SNAPSHOT-runner.jar
