FROM node:14
WORKDIR /app
COPY package.json .
RUN yarn install
COPY . .
EXPOSE 3020
CMD [ "yarn", "start"]

