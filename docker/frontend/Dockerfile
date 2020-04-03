# https://hub.docker.com/_/node
FROM node:12.13.1-alpine

EXPOSE 8000

ADD . /app
WORKDIR /app

RUN yarn
ENTRYPOINT ["yarn", "start", "--env.BACKEND=http://backend:8000", "--host", "0.0.0.0"]
