FROM adoptopenjdk:11.0.8_10-jre-hotspot-bionic@sha256:24864d2d79437f775c70fd368c0272a1579a45a81c965e5fdcf0de699c15a054

RUN set -ex; \
  export DEBIAN_FRONTEND=noninteractive; \
  apt-get update \
  mkdir -p /opt/eventsim

WORDDIR /opt/eventsim

COPY eventsim.sh /opt/eventsim
COPY ../target/scala-2.12/eventsim-assembly-2.0.jar /opt/eventsim
ENTRYPOINT ["eventsim.sh"]
