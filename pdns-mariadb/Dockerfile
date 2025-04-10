
FROM debian:bookworm-slim

ENV MYSQL_ROOT_PASSWORD=rootpass
ENV MYSQL_DATABASE=powerdns
ENV MYSQL_USER=pdns
ENV MYSQL_PASSWORD=pdnspass

RUN apt-get update && apt-get install -y mariadb-server && \
    rm -rf /var/lib/apt/lists/*

COPY pdns-entrypoint.sh /pdns-entrypoint.sh
RUN chmod +x /pdns-entrypoint.sh

EXPOSE 3306
ENTRYPOINT ["/pdns-entrypoint.sh"]
