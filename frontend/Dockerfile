# Step 1: Build the frontend app
FROM node:16-alpine as build
WORKDIR /app
COPY . .
RUN npm install
RUN npm run build

# Step 2: Serve the built app with Nginx
FROM nginx:alpine
COPY nginx.conf /etc/nginx/nginx.conf
COPY --from=build /app/build /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
