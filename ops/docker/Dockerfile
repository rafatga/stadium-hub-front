FROM node:21-alpine

# Set working directory
WORKDIR /app

# Install system dependencies
RUN apk update && apk upgrade

# Copy package.json and package-lock.json
COPY package*.json .

# Copy source code
COPY . .

# Install all dependencies, including dev dependencies
RUN npm install

# Expose port
EXPOSE 3000

CMD [ "npm", "run", "dev" ]
