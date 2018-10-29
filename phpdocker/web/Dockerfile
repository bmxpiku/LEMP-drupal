FROM nginx:latest

RUN apt-get update && \
	apt-get upgrade && \
    apt-get install -y mc && \
    apt-get install -y \
        bzip2 \
        nano \
        telnet \
        wget \
        mysql-client
		
# Install git
RUN apt-get -y install git \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*