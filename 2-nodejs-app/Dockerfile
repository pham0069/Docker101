## docker build .
## docker run -p 3000:80 <id>

# create image based on the image 'node'
FROM node

# specify the working directory on container
WORKDIR /app

# copy package.json first to run npm install (before copying the whole folder to app)
# this is to optimize such that when there's node code change (not dependencies change),
# we dont have to re-run npm install
COPY package.json /app
# run npm install to get the project dependencies
RUN npm install

# copy all the files from the current directory on hosting machine (containing this Dockerfile)
# to the specified directory on container (in this case /app folder)
COPY . /app

# optional, to document that the process in the container will expose this port
EXPOSE 80

# run this command when starting this container
CMD ["node", "server.js"]