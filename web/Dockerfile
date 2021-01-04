FROM node:12-slim

WORKDIR /home/node/apps/web

RUN mkdir -p /home/node/apps/web/node_modules && chown -R node:node /home/node/apps

COPY ./web/package*.json ./

USER node

RUN npm install

COPY --chown=node:node ./web .

CMD ["npm", "run", "start"]
