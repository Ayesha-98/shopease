# Use the official Node.js image as a parent image
FROM node:14

# Set the working directory in the container
WORKDIR /usr/src/app

# Copy package.json and package-lock.json specifically for frontend
COPY frontend/package*.json frontend/

# Install dependencies in the frontend directory
RUN npm install --prefix frontend

# Copy the rest of the application code from the frontend directory
COPY frontend/ frontend/

# Expose the application port (3000 in this case, typical for React apps)
EXPOSE 3000

# Command to run the application, using npm start with the frontend directory specified
CMD ["npm", "start", "--prefix", "frontend"]
