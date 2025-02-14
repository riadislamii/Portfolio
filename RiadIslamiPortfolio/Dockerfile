# Use OpenJDK as the base image
FROM openjdk:17-jdk-slim

# Set the maintainer (optional)
LABEL authors="lenovo"

# Set the working directory inside the container
WORKDIR /app

# Copy the JAR file into the container (ensure the correct path)
COPY target/PortfolioRiadIslami.jar app.jar

# Expose the port (Render assigns it dynamically)
EXPOSE 10000

# Start the application with the correct port from Render
ENTRYPOINT ["sh", "-c", "java -jar -Dserver.port=${PORT} app.jar"]
