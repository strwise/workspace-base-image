#
#--------------------------------------------------------------------------
# Image Setup
#--------------------------------------------------------------------------
#

FROM ghcr.io/linuxserver/baseimage-ubuntu:noble

# set version label
ARG BUILD_DATE
ARG VERSION
ARG CODE_RELEASE
LABEL build_version="StreamWise Workspace version:- ${VERSION} Build-date:- ${BUILD_DATE}"
LABEL org.opencontainers.image.description="StreamWise Workspace Base Image for StreamWise white-label video conferencing platform"
LABEL maintainer="andrekutianski"

# environment settings
ARG DEBIAN_FRONTEND="noninteractive"
ENV HOME="/config"

RUN locale-gen en_US.UTF-8

ENV LANGUAGE=en_US.UTF-8
ENV LC_ALL=en_US.UTF-8
ENV LC_CTYPE=en_US.UTF-8
ENV LANG=en_US.UTF-8
ENV TERM=xterm

# Install runtime dependencies
RUN set -eux && \
    echo "DPkg::options { \"--force-confdef\"; };" >> /etc/apt/apt.conf && \
    echo "**** install runtime packages ****" && \
    apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y \
        bash \
        curl \
        git \
        jq \
        libxml2-utils \
        locales \
        nano \
        postgresql-client \
        rsync \
        sqlite3 \
        tree \
        unzip \
        vim \
        sudo \
        net-tools \
        libatomic1 \
        pkg-config \
        libcurl4-openssl-dev \
        libedit-dev \
        libssl-dev \
        libxml2-dev \
        xz-utils \
        libsqlite3-dev

RUN set -eux \
    # Add the "PHP 8" ppa
    && apt-get install -y software-properties-common \
    && add-apt-repository -y ppa:ondrej/php \
    #
    #--------------------------------------------------------------------------
    # Software's Installation
    #--------------------------------------------------------------------------
    #
    # Install "PHP Extentions", "libraries", "Software's"
    && apt-get update \
    && apt-get upgrade -y \
    && apt-get install -y \
        php8.2-cli \
        php8.2-common \
        php8.2-curl \
        php8.2-intl \
        php8.2-xml \
        php8.2-mbstring \
        php8.2-mysql \
        php8.2-pgsql \
        php8.2-sqlite \
        php8.2-sqlite3 \
        php8.2-zip \
        php8.2-bcmath \
        php8.2-memcached \
        php8.2-gd \
        php8.2-dev && \
    #####################################
    # Composer:
    #####################################
    # Install composer and add its bin to the PATH.
    curl -s http://getcomposer.org/installer | php && \
    echo "export PATH=${PATH}:/var/www/vendor/bin" >> ~/.bashrc && \
    mv composer.phar /usr/local/bin/composer && \
    printf "StreamWise Workspace version: ${VERSION}\nBuild-date: ${BUILD_DATE}" > /build_version && \
    echo "**** clean up ****" && \
    apt-get clean && \
    rm -rf \
    /config/* \
    /tmp/* \
    /var/lib/apt/lists/* \
    /var/tmp/*


 