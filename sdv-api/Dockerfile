FROM rust:1.82.0 AS builder

WORKDIR /usr/src/app

COPY . .

RUN cargo build --release

FROM debian:latest

WORKDIR /usr/src/app

# RUN apt-get update & apt-get install -y extra-runtime-dependencies & rm -rf /var/lib/apt/lists/*

COPY --from=builder /usr/src/app/target/release/sdv-api /usr/local/bin/sdv-api

EXPOSE 8000

CMD ["/usr/local/bin/sdv-api"]
