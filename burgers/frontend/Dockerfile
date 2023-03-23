FROM node:alpine

ENV NODE_ENV production
ENV PORT 3000


# ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"] 
# RUN chmod +x usr/local/bin/docker-entrypoint.sh

# TODO: add the Docker commands to do these steps:

# at build time:
# set the current directory to `/src`
WORKDIR /src 

# copy the manifest file: package.json
COPY package.json /src

# from a shell, run `npm install`
RUN npm install 

# copy the content into place
COPY . /src

# let traffic flow in on port 3000
EXPOSE 3000

# set the environment variable `BACKEND` to `http://backend:5000`
ENV BACKEND http://burgerback:5000

# as the container starts:
# `npm start`
CMD [ "npm","start" ]
