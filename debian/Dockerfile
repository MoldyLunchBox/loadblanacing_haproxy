FROM debian
run apt update -y && apt install haproxy -y
RUN mv /etc/haproxy/haproxy.cfg /etc/haproxy/haproxy.cfg.bak
COPY ./haproxy/haproxy.cfg /etc/haproxy
ENTRYPOINT ["/bin/bash", "-c", "/etc/init.d/haproxy restart && tail -f /dev/null"]