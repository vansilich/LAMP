FROM php:5.5.38-fpm-alpine

# Install tools required for build stage
RUN apk add --update --no-cache \
    bash curl wget rsync ca-certificates openssl openssh git tzdata openntpd \
    libxrender fontconfig libc6-compat \
    mysql-client binutils-gold autoconf \
    g++ gcc gnupg libgcc linux-headers make python zlib-dev

RUN docker-php-ext-configure zip --with-libzip
# Install additional PHP libraries
RUN docker-php-ext-install bcmath pdo_mysql mysql mysqli zip

EXPOSE 9000