# Use an official Node runtime as the base image
FROM node:18-bullseye

# Set the working directory in the container
WORKDIR /storybook

# Copy the rest of the application code
COPY . .

# Install dependencies
RUN npm install

# Run type-check
RUN npm run type-check

# Start the development server
CMD ["npm", "start"]