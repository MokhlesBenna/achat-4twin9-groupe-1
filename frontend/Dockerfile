# Stage 1: Build Angular app (Optional if already built with ng build)
# FROM node:18-alpine AS builder
# WORKDIR /app
# COPY . .
# RUN npm install
# RUN npm run build -- --configuration production

# Stage 2: Serve with nginx
FROM nginx:alpine

# Remove default nginx static files
RUN rm -rf /usr/share/nginx/html/*

# Copy the built Angular app (adjust path if needed)
COPY dist/achat-frontend /usr/share/nginx/html

# Expose port 80
EXPOSE 80

# Start nginx
CMD ["nginx", "-g", "daemon off;"]
