# Use official Node.js 18 Alpine image as the base image
FROM node:18-alpine

# Set the working directory in the container
WORKDIR /frontend

# Copy package.json and package-lock.json to leverage Docker cache
COPY package.json ./
COPY package-lock.json ./

# Install dependencies using --legacy-peer-deps to resolve peer dependency conflicts
RUN npm install --silent

# Copy the application files
COPY public/ ./public
COPY src/ ./src

# Expose the port the app runs on
EXPOSE 3000

# Start the application
CMD ["npm", "start"]