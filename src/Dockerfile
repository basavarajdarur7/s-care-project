# Use an official Node.js runtime as a base image
FROM node:14

# Set the working directory in the container
WORKDIR /usr/src/app

# Copy package.json and package-lock.json to the working directory
COPY package*.json ./

# Install the application dependencies
RUN npm install

# Copy the remaining application code to the working directory
COPY . .

# Build the React app for production
RUN npm run build

# Expose the port that the app will run on (assumes your app runs on port 80)
EXPOSE 80

# Start the application
CMD ["npm", "start"]
