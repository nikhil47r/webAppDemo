# syntax=docker/dockerfile:1

FROM node:20-alpine as builder
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .

FROM node:20-alpine
WORKDIR /app
COPY --from=builder /app /app
USER node
ENV NODE_ENV=production
CMD ["node", "src/index.js"]
