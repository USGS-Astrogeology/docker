FROM docker:19.03.13-dind

ENV PIP_CERT /etc/ssl/certs/ca-certificates.crt

COPY DOIRootCA2.crt /usr/local/share/ca-certificates/
COPY DigiCertCA.crt /usr/local/share/ca-certificates/ 
RUN update-ca-certificates

RUN apk add \
    cargo \
    gcc \
    libc-dev \
    libffi-dev \
    make \
    openssl-dev \
    py-pip \
    python3-dev \
    rust 

RUN pip install -U docker-compose

