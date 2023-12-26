FROM rust:1.74.0-slim-bookworm as builder
RUN apt update -y && apt install build-essential -y --no-install-recommends

FROM builder
RUN cargo install cobalt-bin

WORKDIR /home/thall/code/projects/thallheim.com
RUN mkdir -p dest
COPY . .
ENTRYPOINT ["cobalt", "build"]
