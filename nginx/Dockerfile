# Use a specific version of NGINX as the base image
FROM nginx:latest

# Copy the custom configuration file to conf.d

COPY nginx.conf /etc/nginx/conf.d/default.conf
# Expose port 4500
EXPOSE 4500

# Start NGINX when the container runs
CMD ["nginx", "-g", "daemon off;"]

