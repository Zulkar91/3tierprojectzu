FROM node:21-alpine AS builder
WORKDIR /app
COPY package*.json .
RUN npm install
COPY . .
FROM node:21-alpine
WORKDIR /app
COPY --from=builder /app /app
COPY .env .env
EXPOSE 8080
CMD ["npm", "start"]
