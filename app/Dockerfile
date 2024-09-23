# Use Node.js as the base image
FROM node:16

# Set the working directory
WORKDIR /app

# Install app dependencies
COPY package*.json ./
RUN npm install

# Copy the app source code
COPY . .

# Update Browserslist database
RUN npx update-browserslist-db@latest --update-db

# Build the React app for production with openssl-legacy-provider flag
RUN npm run build --openssl-legacy-provider


# Expose port 3000 for the React app
EXPOSE 3000

# Serve the app using the 'serve' package
CMD ["npm", "run", "Start"]