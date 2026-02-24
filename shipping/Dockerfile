FROM maven:4.0.0-rc-5-eclipse-temurin-17-alpine As builder
WORKDIR /app/server
COPY pom.xml .
COPY src /app/server/src
RUN mvn clean package 



FROM eclipse-temurin:17-jre-alpine
RUN addgroup -S roboshop && adduser -S roboshop -G roboshop
WORKDIR /app/server
USER roboshop
COPY --from=builder /app/server/target/shipping-*.jar /app/server/shipping.jar
CMD ["java","-jar", "shipping.jar"]