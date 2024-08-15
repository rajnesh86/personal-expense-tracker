# Use an official OpenJDK runtime as the base image
FROM openjdk:21-jdk-slim

# Set the working directory in the container
WORKDIR /app

# Copy the built jar file into the container
COPY target/api-gateway-1.0-SNAPSHOT.jar api-gateway.jar

# Expose the port that the API Gateway runs on
EXPOSE 8080

# Command to run the API Gateway
ENTRYPOINT ["java", "-jar", "api-gateway.jar"]
