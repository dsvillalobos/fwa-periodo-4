# Step 1: Use an official Node.js runtime as the base image
FROM node:20-alpine

# Step 2: Set the working directory inside the container
WORKDIR /app

# Step 3: Copy the package.json and package-lock.json files to the container
COPY package*.json ./

# Step 4: Install the project dependencies
RUN npm install

# Step 5: Copy the rest of the application source code to the container
COPY . .

# Step 6: Build the Vite project
RUN npm run build

# Step 7: Expose port 4000 to the outside world
EXPOSE 44

# Step 8: Set environment variables for Vite
ENV PORT=44

# Step 9: Run the Vite app
CMD ["npm", "run", "preview"]
