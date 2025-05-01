# The FROM instruction specifies the base image that the container will be built on top of. 
# This instruction is typically the first one in a Dockerfile and is used to set the base image for the container. 
# This instruction tells Docker to use the node:22-slim image as the base image for the container. 
# To use a specific version or tag of an image you can use:<version> or:<tag> syntax.
FROM node:22-slim

# In a Dockerfile, the WORKDIR instruction sets the working directory for any command that follows it in the Dockerfile. 
# This means that any commands that are run in the container will be executed relative to the specified directory. 
# This instruction tells Docker to set the working directory of the container to /app . 
# Any subsequent commands in the Dockerfile, such as COPY, RUN, or CMD, will be executed in this directory.
WORKDIR /app

# Use the COPY instruction to copy local files from the host machine to the current working directory. 
# For example, to copy a file named package.json and index.js from the host machine's current directory to the image's /app directory.
COPY package.json /app/
COPY index.js /app/
# If you want to copy all the files from the host's current directory to the container's current directory/
# The first "." refers to the source directory on the host machine, and the second "." refers to the destination directory within the container.
# COPY . . 

# Use the "RUN" instruction to execute commands that will run during the image build process.
# To update the package manager and install a specific package, you would use
RUN npm install

# In a Dockerfile, the CMD instruction sets the command that will be executed when a container is run from the image.
# This instruction tells Docker to run the command npm start when a container is created from the image.
CMD ["npm", "start"]

# Use the ENV instruction to set environment variables inside the image which will be available during build time as well as in a running container.
ENV NODE_ENV=production

# Use the EXPOSE command to tell Docker which ports the container will listen on at runtime.
EXPOSE 3000
