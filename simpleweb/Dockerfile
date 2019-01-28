# Specify base img
FROM node:alpine

WORKDIR /usr/app
# install dependencies
COPY ./package.json ./

# Proxy config (remove if not necessary)
RUN npm config set proxy http://localhost:3128 install
COPY ./ ./

# Default cmd 
CMD ["npm", "start"]