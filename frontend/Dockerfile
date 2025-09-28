# Use Nginx to serve the frontend
FROM nginx:alpine

# Copy custom Nginx configuration
COPY nginx.conf /etc/nginx/nginx.conf

# Copy frontend static files into the container
COPY . /usr/share/nginx/html

# Expose port 80 (Nginx default)
EXPOSE 80

# Start Nginx in foreground
CMD ["nginx", "-g", "daemon off;"]
