# Use the official Node.js 18 image based on Alpine Linux for a lightweight build
FROM node:18-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy the package.json and package-lock.json files to the working directory
COPY package*.json ./

# Install the dependencies defined in package.json
RUN npm install

# Copy all files from the local system to the working directory
COPY . .

# Build the Nuxt.js application
RUN npm run build

# Expose port 3000 to accept incoming requests
EXPOSE 3000

# Default command to start the Nuxt.js application
CMD ["npm", "run", "start"]
