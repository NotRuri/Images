FROM debian:bookworm-slim

LABEL version="1.0" \
      description="Debian base installer" \
      author="Ruri" \
      maintainer="github.com/NotRuri"

RUN apt-get update -qy && \
    apt-get install -qy wget curl unzip tar jq && \
    apt-get clean
