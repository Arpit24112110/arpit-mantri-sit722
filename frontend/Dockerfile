# Use Nginx to serve the frontend
FROM nginx:alpine

# Copy custom Nginx configuration (if you have one)
COPY nginx.conf /etc/nginx/nginx.conf

# Copy frontend static files into the container
COPY . /usr/share/nginx/html

# Expose port 3000 to match docker-compose and pipeline
EXPOSE 3000

# Start Nginx in foreground
CMD ["nginx", "-g", "daemon off;"]
