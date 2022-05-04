FROM node:14-alpine as build
WORKDIR /usr/src/app
COPY *.json ./
Run npm install
COPY . ./
RUN npm run build

FROM nginx:1.12.0-alpine
COPY ./nginx.conf /etc/nginx/nginx.conf
COPY --from=build /usr/src/app/build /usr/share/nginx/html/bookstore
EXPOSE 80
