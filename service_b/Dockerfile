# Use the official PHP 8.2 image as the base image
FROM php:8.2-apache

# Set the working directory inside the container
WORKDIR /var/www/html/service_b

# Copy the contents of the current directory to the working directory inside the container
COPY . /var/www/html/service_b

# Expose port 80
EXPOSE 80

RUN apt-get update && apt-get install -y default-mysql-client
RUN docker-php-ext-install pdo_mysql

# Start Apache in the foreground
CMD ["apache2-foreground"]