# FROM node:22
# WORKDIR /app
# COPY package*.json ./
# RUN npm install
# # COPY . .
# EXPOSE 5174
# CMD ["npm","run","dev","--","--host","0.0.0.0"]

# Stage 1: Build React
FROM node:22 AS builder

WORKDIR /app

COPY package*.json ./

RUN npm ci

COPY . .

RUN npm run build


# Stage 2: Serve React with Nginx
FROM nginx:alpine

COPY --from=builder /app/dist /usr/share/nginx/html

EXPOSE 80