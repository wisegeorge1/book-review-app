# Use Node.js LTS as base image
FROM node:20-alpine

# Set working directory
WORKDIR /app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm ci --omit-dev

# Copy the rest of the application files
COPY . .

# Expose the port the backend runs on
EXPOSE 3001

# Start the backend server
CMD ["node", "src/server.js"]

