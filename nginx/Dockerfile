# Use a specific version of NGINX as the base image
FROM nginx:1.23.4
# Copy the custom sites-available configuration file
COPY nginx.conf /etc/nginx/conf.d/default.conf
EXPOSE 4500
# Start NGINX when the container runs
CMD ["nginx", "-g", "daemon off;"]
