FROM node:alpine as builder
WORKDIR '/app'
COPY package.json .
RUN npm config set proxy http://172.17.0.1:3128 install
COPY . .
RUN npm run build

FROM nginx
COPY --from=builder /app/build /usr/share/nginx/html
