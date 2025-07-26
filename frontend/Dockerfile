# Stage 1: Build react app

FROM node:18-alpine AS build

# To set environmant variable
ENV NODE_OPTIONS=--openssl-legacy-provider

WORKDIR /app

COPY package*.json ./

RUN npm install

# Ensure required packages are installed
RUN npm install react react-dom react-scripts axios

COPY . .
RUN npm run build

# Stage 2: Serve with Nginx
FROM nginx:alpine

COPY --from=build /app/build /usr/share/nginx/html

COPY nginx.conf /etc/nginx/conf.d/default.conf
# Copy the custom Nginx configuration file
# Ensure you have a nginx.conf file in the same directory as this Dockerfile
# or adjust the path accordingly

EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]