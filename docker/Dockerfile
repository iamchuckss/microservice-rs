
FROM rustlang/rust:nightly
MAINTAINER <schuck017@gmail.com>

ENV SSL_CERT_FILE=/etc/ssl/certs/ca-certificates.crt

# Install vim for in-place editing.
RUN apt-get update -y && apt-get install -y vim

WORKDIR /var/www/microservice/
COPY . .

RUN rustc --version
RUN cargo build

RUN cargo run