FROM node:lts-slim
LABEL maintainer="Lucas Santos <lucassm02@gmail.com>"


ARG NODE_ENV=development
ENV NODE_ENV=${NODE_ENV} 

WORKDIR /app
COPY package.json .
RUN yarn install

COPY . .
EXPOSE 3020
CMD [ "yarn", "start"]

