FROM node:12-slim

WORKDIR /home/node/apps/api

RUN apt-get update -qq && apt-get install -y procps

RUN mkdir -p /home/node/apps/api/node_modules && chown -R node:node /home/node/apps/api

COPY ./api/package*.json ./

USER node

RUN npm install

COPY --chown=node:node ./api .

CMD ["npm", "run", "start:dev"]
