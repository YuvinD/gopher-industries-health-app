# Use an official OpenJDK runtime as a parent image
FROM openjdk:17-jdk-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy the JAR file from the host machine (your project) to the Docker container
COPY target/health-app-1.0-SNAPSHOT.jar /app/health-app.jar

# Run the JAR file inside the container
CMD ["java", "-jar", "/app/health-app.jar"]
