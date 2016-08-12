FROM fedora

RUN dnf install -y \
	    emacs-nox \
	    curl \
	    openssh-clients && \
    dnf clean all  && \
    mkdir -p /root/.ssh && \
    curl http://autotest.qa.sw.ru/pub/qanet-rsa > /root/.ssh/id_rsa && \
    chmod 700 /root/.ssh/id_rsa && \
    sed -i \
        -e '$a UserKnownHostsFile /dev/null' \
        -e '$a StrictHostKeyChecking no' \
                /etc/ssh/ssh_config
