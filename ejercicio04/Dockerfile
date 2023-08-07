# Use the official OpenJDK base image to run Java applications
FROM openjdk:11-jre-slim

# Copy the .jar file into the container
COPY passwordapi.jar /app/passwordapi.jar

# Set the working directory to /app
WORKDIR /app

# Expose port 8080 to the host
EXPOSE 8080

# Command to run the .jar file
CMD ["java", "-jar", "passwordapi.jar"]
