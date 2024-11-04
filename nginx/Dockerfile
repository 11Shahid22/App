
# Use the official NGINX image as the base image
FROM nginx:latest

# Create the sites-available and sites-enabled directories
RUN mkdir -p /etc/nginx/sites-available /etc/nginx/sites-enabled

# Copy the custom sites-available configuration file
COPY nginx.conf /etc/nginx/sites-available/

# Create a symlink from sites-available to sites-enabled
RUN ln -s /etc/nginx/sites-available/nginx.conf /etc/nginx/sites-enabled/

# Create a custom nginx.conf that includes the sites-enabled directory
RUN echo 'worker_processes 1 ;\n\
events { worker_connections 1024; }\n\
http {\n\
    include /etc/nginx/sites-enabled/*.conf;\n\
}' > /etc/nginx/nginx.conf
# Expose port 80
EXPOSE 4500

