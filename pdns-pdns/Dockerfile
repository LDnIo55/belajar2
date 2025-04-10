
FROM debian:bookworm-slim

RUN apt-get update && \
    apt-get install -y pdns-server pdns-backend-mysql && \
    rm -rf /var/lib/apt/lists/*

COPY pdns.conf /etc/powerdns/pdns.conf

EXPOSE 53/udp
EXPOSE 53/tcp

CMD ["pdns_server", "--daemon=no", "--guardian=no"]
