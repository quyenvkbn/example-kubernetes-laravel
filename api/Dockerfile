# Set master image
#FROM php:8.0-fpm
FROM php:8.0-fpm-alpine

LABEL maintainer="demo <demo@gmail.com>"

RUN docker-php-ext-install pdo_mysql bcmath tokenizer ctype fileinfo
	
# Set working directory
WORKDIR /var/www/laravel-app

# Install PHP Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# Copy existing application directory
COPY . .