# vim: ft=dockerfile

FROM ubuntu:18.04

RUN apt-get update &&                       \
    apt-get install -y ca-certificates &&   \
    rm -rf /var/lib/apt/lists/* &&          \
    rm -rf /var/cache/apt/*
COPY DOIRootCA2.crt /usr/local/share/ca-certificates/ 
COPY DigiCertCA.crt /usr/local/share/ca-certificates/ 
RUN update-ca-certificates

RUN mkdir -p /docker-entrypoint.d
COPY docker-entrypoint.sh /
RUN chmod +x /docker-entrypoint.sh
ENTRYPOINT ["/bin/bash", "/docker-entrypoint.sh"]


