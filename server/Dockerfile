# Use Node.js as the base image
FROM node:16

# Create app directory
WORKDIR /app

# Install app dependencies
COPY package*.json ./
RUN npm install

# Copy the app source code
COPY . .

# Expose port 5050
EXPOSE 5050

# Start the server
CMD ["npm", "run", "dev"]