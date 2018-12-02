FROM mysql:8.0

RUN apt-get update && \
	apt-get upgrade && \
    apt-get install -y mc && \
    apt-get install -y \
        bzip2 \
        nano \
		procps \
		
RUN apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*
	
RUN mysql --user=root --password=root --execute="ALTER USER 'root'@'%' IDENTIFIED WITH mysql_native_password BY 'root';"