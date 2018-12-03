FROM nginx:latest

RUN apt-get update && \
	apt-get upgrade -y && \
    apt-get install -y mc && \
    apt-get install -y \
        bzip2 \
        nano \
		curl \
        telnet \
        wget \
        mysql-client \
		pv \
		procps

# Install git
RUN apt-get -y install git \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*

ADD .bash_profile /root/
ADD drupal7.conf /etc/nginx/
ADD drupal8.conf /etc/nginx/

COPY conf.d/ /etc/nginx/conf.d/
