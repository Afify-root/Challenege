# Use the PHP 8.1 image with FPM (FastCGI Process Manager)
FROM php:8.1-fpm

# Update the package list and install required dependencies
RUN apt-get update && apt-get install -y \
    libpng-dev \           # Library to support PNG images
    libjpeg-dev \          # Library to support JPEG images
    libfreetype6-dev \     # Library to support TrueType fonts
    zip \                  # Install the Zip compression tool
    unzip \                # Install the Zip extraction tool
    git \                  # Install Git for version control
    && docker-php-ext-install pdo_mysql gd # Install PHP extensions for PDO and GD

# Copy Composer from the official Composer image to the appropriate path in the image
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

# Set the working directory inside the container
WORKDIR /var/www

# Copy all files from the local system to the working directory
COPY . /var/www

# Install dependencies from the composer.json file with optimization
RUN composer install --no-dev --optimize-autoloader

# Change ownership of the files in the directory to the www-data user
RUN chown -R www-data:www-data /var/www

# Expose port 8000 to accept incoming requests
EXPOSE 8000

# Default command to run PHP-FPM
CMD ["php-fpm"]
