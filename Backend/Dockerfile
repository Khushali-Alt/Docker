#-----Stage 1----Build stage
FROM node:24.14.0-alpine AS builder

WORKDIR /app

COPY package*.json ./

RUN npm install 

COPY . .

#---- Start 2--- Production Stage
FROM node:24.14.0-alpine

WORKDIR /app

COPY --from=builder /app /app

EXPOSE 3000

ENV PORT=3000

CMD ["node" ,"index.js"]