FROM maven
WORKDIR /app/server
COPY pom.xml .
COPY src/ /app/server/src
RUN mvn clean package 
RUN mv /app/server/target/shipping-1.0.jar /app/server/shipping.jar
CMD ["java","-jar", "shipping.jar"]