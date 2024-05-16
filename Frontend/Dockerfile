# Use the official Node.js image as a base image
FROM node:14

# Set the working directory inside the container
WORKDIR /SPE/Final_Project/SPE-Final-Project/Frontend

# Copy package.json and package-lock.json files to the working directory
COPY package*.json ./

# Install the dependencies
RUN npm install

# Copy the rest of the application code to the working directory
COPY . .

# Build the React application
RUN npm run build

# Install a simple HTTP server to serve the built files
RUN npm install -g serve

# Expose the port the application will run on
EXPOSE 5173

# Command to run the application
CMD ["serve", "-s", "build"]

# FROM openjdk:17
# COPY ./target/Calculator_MT2023085-0.0.1-SNAPSHOT.jar ./
# WORKDIR ./
# CMD [“java”,”-jar”,” Calculator_MT2023085-0.0.1-SNAPSHOT.jar”]