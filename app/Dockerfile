# dev
FROM node:18-alpine AS dev
RUN apk add --no-cache tzdata
ENV TZ Asia/Novosibirsk
ENV NODE_PATH /opt/server/node_modules

WORKDIR /opt/server/

CMD [ "node" ]

# production
FROM node:18-alpine AS production
RUN apk add --no-cache tzdata
ENV TZ Asia/Novosibirsk
ENV NODE_PATH /opt/server/node_modules

WORKDIR /opt/server/

COPY /*.json ./
RUN npm i

CMD ["sh", "-c", "npm run start"]