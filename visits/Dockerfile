FROM node:alpine
ENV http_proxy http://127.0.0.1:3128
ENV https_proxy http://127.0.0.1:3128

WORKDIR '/app'

COPY package.json .
RUN npm config set proxy http://localhost:3128 install
COPY . .

CMD ["npm", "start"]