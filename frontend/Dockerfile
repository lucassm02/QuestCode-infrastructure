FROM node:lts-slim as builder
LABEL maintainer="Lucas Santos <lucassm02@gmail.com>"
WORKDIR /builder

COPY package.json .
RUN yarn install

COPY /src ./src
COPY /public ./public
RUN yarn build

FROM nginx:1.21.0
COPY --from=builder /builder/build  /usr/share/nginx/html
EXPOSE 80