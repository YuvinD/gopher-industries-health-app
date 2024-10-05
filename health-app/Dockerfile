# Use OpenJDK 17
FROM openjdk:17-jdk-alpine

# Set the working directory
WORKDIR /app

# Copy the JAR file of your application into the image
COPY target/health-app-1.0-SNAPSHOT.jar /app/health-app.jar

# Copy the New Relic agent into the Docker image
COPY newrelic/newrelic.jar /app/newrelic.jar
COPY newrelic/newrelic.yml /app/newrelic.yml

# Run the application with the New Relic agent
CMD ["java", "-javaagent:/app/newrelic.jar", "-jar", "/app/health-app.jar"]
