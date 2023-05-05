# Use an official Node.js runtime as a parent image
FROM node:16-alpine

# Set the working directory to /frontend
WORKDIR /frontend

# Copy the package.json and package-lock.json files to the container
COPY package*.json ./

# Install the frontend dependencies
RUN npm install

# Copy the rest of the frontend code to the container
COPY . .

# Build the frontend app
RUN npm run build

# Expose port 80 for the frontend app
EXPOSE 80

# Start the frontend app
CMD ["npm", "run", "dev"]
