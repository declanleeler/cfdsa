# get node 21 base image
FROM node:21

# create /app folder and cd into it
WORKDIR /app

# inside /app

# copy files into folder, except dependencies
COPY main.js .
COPY package.json .
COPY package-lock.json .
COPY public public
COPY views views

# install dependencies
RUN npm ci

# run
ENV PORT=3000
ENV INSTANCE_NAME="Hello"
ENV INSTANCE_HASH="123"

EXPOSE ${PORT}

ENTRYPOINT node main.js 
