# Step 1: Use an official lightweight Nginx image from Docker Hub
FROM nginx:alpine

# Step 2: Copy your local HTML file into the default Nginx web directory
COPY index.html /usr/share/nginx/html/index.html

# Step 3: Inform Docker that the container listens on port 80 at runtime
EXPOSE 80