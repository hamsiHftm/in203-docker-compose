# Use the official Node.js runtime as the base image
FROM node:14-alpine

# Set the working directory in the container
WORKDIR /app

# Copy the package.json and package-lock.json files into the container
# express needs package.json to run, so its needed to be copy in container
COPY package*.json ./

# Install the dependencies in the container
# node-modules needs to be install to start the app
RUN npm install
RUN npm install cors

# Copy the rest of the frontend source code into the container
COPY . .

# Specifying the port
EXPOSE 3001

# Set the command to run the application
CMD [ "node", "app.js" ]
