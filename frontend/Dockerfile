FROM node:14 as builder
WORKDIR /builder
COPY package.json .
RUN yarn install
COPY /src ./src
COPY /public ./public
RUN yarn build


FROM nginx:1.21.0
COPY --from=builder /builder/build  /usr/share/nginx/html
EXPOSE 80