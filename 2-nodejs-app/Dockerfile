## docker build .
## docker run -p 3000:80 <id>

# create image based on the image 'node'
FROM node

# specify the working directory on container
WORKDIR /app

# copy all the files from the current directory on hosting machine (containing this Dockerfile)
# to the specified directory on container (in this case /app folder)
COPY . /app

# run this command when creating this image
RUN npm install

# optional, to document that the process in the container will expose this port
EXPOSE 80

# run this command when starting this container
CMD ["node", "server.js"]