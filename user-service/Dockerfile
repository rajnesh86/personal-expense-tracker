# Use an official OpenJDK runtime as a parent image
FROM openjdk:21-jdk-slim

# Set the working directory in the container
WORKDIR /app

# Copy the JAR file built by Maven/Gradle into the container
COPY target/user-service-1.0-SNAPSHOT.jar user-service.jar

# Expose the port the application will run on
EXPOSE 8081

# Command to run the Spring Boot application
ENTRYPOINT ["java", "-jar", "user-service.jar"]
