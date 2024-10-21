FROM rust:1.82.0 AS builder

WORKDIR /usr/src/app

COPY . .

RUN cargo build --release

FROM debian:latest

WORKDIR /usr/local/bin

# RUN apt-get update & apt-get install -y extra-runtime-dependencies & rm -rf /var/lib/apt/lists/*

COPY --from=builder /usr/src/app/target/release/sdv-api /usr/local/bin/sdv-api

ENV ROCKET_ADDRESS="0.0.0.0"
ENV ROCKET_PORT="8000"

EXPOSE 8000

CMD ["/usr/local/bin/sdv-api"]
