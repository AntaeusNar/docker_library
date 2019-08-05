FROM selenium/standalone-firefox-debug

USER root

RUN sudo apt-get update -qqy \
  && sudo apt-get -qqy install \
  python pip \
  && rm -rf /var/lib/apt/lists/* /var/cache/apt/*

USER seluser
