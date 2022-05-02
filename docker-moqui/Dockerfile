FROM tomcat:9.0.62-jre11-temurin-focal
LABEL maintainer="Oliver Kroener <ok@oliver-kroener.de>"

# Install snakeoil certificate 
RUN \
    apt-get update && \
    apt-get install -y perl && \
    apt-get install libterm-readline-gnu-perl -y && \
    apt-get install -y dialog apt-utils && \
    apt-get upgrade -y && \
    apt-get install -y ssl-cert && \
    make-ssl-cert generate-default-snakeoil --force-overwrite && \
# Cleanup
    rm -rf /var/lib/apt/lists/* /usr/src/*
