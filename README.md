**How to Run eureka-server**
 
 **Step 1: Create a Dockerfile Using JDK 21**
    # Use an official JDK 21 runtime as the base image
    FROM openjdk:21-jdk-slim
    
    # Set the working directory in the container
    WORKDIR /app
    
    # Copy the built jar file into the container
    COPY target/eureka-server-1.0-SNAPSHOT.jar eureka-server.jar
    
    # Expose the port Eureka Server runs on
    EXPOSE 8761
    
    # Command to run the Eureka Server
    ENTRYPOINT ["java", "-jar", "eureka-server.jar"]

**Step 2: Build the Docker Image**
   docker build -t eureka-server .

**Step 3: Run the Docker Container**
  docker run -d -p 8761:8761 --name eureka-server eureka-server

**Step 4: Access the Eureka Server Dashboard**
Once the container is running, open your browser and navigate to http://localhost:8761.
You should see the Eureka Server dashboard.



