FROM selenium/standalone-firefox-debug

USER root

RUN apt-get update -qqy \
  && apt-get -qqy install \
  python pip \
  && rm -rf /var/lib/apt/lists/* /var/cache/apt/*

USER seluser
