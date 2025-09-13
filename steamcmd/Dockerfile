FROM debian:bookworm-slim

LABEL version="1.0" \
      description="Base container for SteamCMD" \
      author="Ruri" \
      maintainer="github.com/NotRuri"

RUN apt-get update && \
    apt-get install -y --no-install-recommends lib32gcc-s1 ca-certificates

RUN useradd -m -s /bin/bash steam

WORKDIR /home/steam

ADD https://steamcdn-a.akamaihd.net/client/installer/steamcmd_linux.tar.gz .

RUN chown -R steam:steam .

USER steam

RUN mkdir steamcmd && \
    tar -xzf steamcmd_linux.tar.gz -C /home/steam/steamcmd && \
    rm steamcmd_linux.tar.gz

WORKDIR /home/steam/steamcmd

ENTRYPOINT ["./steamcmd.sh"]
