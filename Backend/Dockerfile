FROM node:20-alpine

WORKDIR /app

COPY Backend/package*.json ./

RUN npm install

COPY Backend/ .

EXPOSE 4002

ENV NODE_ENV=production

CMD ["npm", "start"]
