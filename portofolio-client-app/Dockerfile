FROM node:20-alpine

# Set the working directory inside the container
WORKDIR /usr/src/app

ENV PORT 8080
ENV HOST 0.0.0.0

# Copy package.json to the working directory
COPY package*.json ./

# Run npm install to install dependencies
RUN npm install -only=production

# Copy local react code to the container
COPY . .

# Build app
RUN npm run build

# Start the service
CMD npm start