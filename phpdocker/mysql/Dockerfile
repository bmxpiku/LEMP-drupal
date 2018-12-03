FROM mysql:8.0

RUN apt-get update && \
	apt-get upgrade && \
    apt-get install -y mc && \
    apt-get install -y \
        bzip2 \
        nano \
		procps \
		
RUN apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*
