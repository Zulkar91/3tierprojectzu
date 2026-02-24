FROM node:21-alpine AS builder
WORKDIR /app
COPY package*.json /app
RUN npm install
COPY . .
FROM node:21-alpine
WORKDIR /app
COPY --from=builder /app /app
COPY .env .env
EXPOSE 5173
CMD ["npm", "start"]
