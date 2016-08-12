FROM debian:latest

RUN apt-get update && \
    apt-get -y install \
	emacs-nox \
	curl \
	openssh-client && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* \
       /usr/share/doc /usr/share/doc-base \
       /usr/share/man /usr/share/locale /usr/share/zoneinfo && \
    \
    mkdir -p /root/.ssh && \
    curl http://autotest.qa.sw.ru/pub/qanet-rsa > /root/.ssh/id_rsa && \
    chmod 700 /root/.ssh/id_rsa && \
    sed -i \
        -e '$a UserKnownHostsFile /dev/null' \
        -e '$a StrictHostKeyChecking no' \
                /etc/ssh/ssh_config
