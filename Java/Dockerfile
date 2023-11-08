# Use an official Java image as the base image
FROM openjdk:11

# Set the working directory inside the container
WORKDIR /app

# Copy the Java application source code into the container
COPY Main.java .

# Compile the Java code
RUN javac Main.java

# Run the Java application
CMD ["java", "Main"]
