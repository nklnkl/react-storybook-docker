# Use an official Node runtime as the base image
FROM node:18-bullseye

# Set the working directory in the container
WORKDIR /storybook

# Install xdg-utils
RUN apt-get update && apt-get install -y xdg-utils

# Copy the rest of the application code
COPY . .

# Install dependencies
RUN npm install

# Run type-check
RUN npm run type-check

# Build Storybook
RUN npm run build-storybook

# Define the command to run Storybook
CMD ["npm", "run", "storybook"]
