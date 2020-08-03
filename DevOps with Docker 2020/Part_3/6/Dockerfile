FROM node:10-alpine as build-stage

USER node
WORKDIR /home/node
ENV NODE_ENV=production

ADD . .

RUN set -x \
  && npm install \
  && npm run build

FROM nginx
COPY --from=build-stage /home/node/dist /usr/share/nginx/html