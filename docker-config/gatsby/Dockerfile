FROM node:15.14-slim

RUN mkdir /app
# https://www.digitalocean.com/community/tutorials/how-to-build-a-node-js-application-with-docker-quickstart
RUN mkdir -p /app/node_modules && chown -R node:node /app

WORKDIR /app

EXPOSE 8000

COPY package*.json *yarn* ./

# RUN mkdir node_modules

# https://www.docker.com/blog/keep-nodejs-rockin-in-docker/
USER node

RUN yarn install --force && yarn cache clean

COPY --chown=node:node app/ .

CMD ["yarn", "run", "gatsby-develop" ]
# CMD ["gatsby", "develop", "-H", "0.0.0.0" ]
# CMD tail -f /dev/null
