# syntax=docker/dockerfile:1

# Use a multi-platform capable base image
FROM --platform=$BUILDPLATFORM node:14 AS base

# Define the working directory
WORKDIR /bezkoder-app

# Copy package.json and install dependencies
COPY package.json .
RUN npm install

# Copy application source code
COPY . .

# Define the default platform
CMD ["npm", "start"]
