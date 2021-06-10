FROM alpine:edge
MAINTAINER jelou
env name jelou
# env pass 123132

RUN apk update && apk add --no-cache openssh
RUN ssh-keygen -A

ADD docker-entrypoint.sh /usr/local/bin
RUN rm -rf /etc/ssh/ssh_host_rsa_key /etc/ssh/ssh_host_dsa_key

#ADD ./sshd_config /etc/ssh/sshd_config
#RUN ssh-keygen -t rsa -b 4096 -f /etc/ssh/ssh_host_rsa_key -N ""
#COPY run.sh /tmp
#ENTRYPOINT ["/tmp/run.sh"]

EXPOSE 22