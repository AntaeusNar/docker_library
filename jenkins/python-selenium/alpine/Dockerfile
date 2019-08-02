# Alphine + Python + Selenium + Firefox + Xvfb
FROM python:3.7.4-alpine3.10

# RUN echo "http://dl-4.alpinelinux.org/alpine/edge/main" >> /etc/apk/repositories && \
#     echo "http://dl-4.aplinelinux.org/alpine/edge/community" >> /etc/apk/repositories

RUN apk update && \
    apk add curl unzip dbus-x11 ttf-freefont \
            firefox-esr xvfb xdpyinfo grep && \
    pip install selenium

RUN GECKODRIVER_VERSION=`curl https://github.com/mozilla/geckodriver/releases/latest | grep -Po 'v[0-9]+.[0-9]+.[0-9]+'` && \
    wget https://github.com/mozilla/geckodriver/releases/download/$GECKODRIVER_VERSION/geckodriver-$GECKODRIVER_VERSION-linux64.tar.gz && \
    tar -zxf geckodriver-$GECKODRIVER_VERSION-linux64.tar.gz -C /usr/local/bin && \
    chmod +x /usr/local/bin/geckodriver && \
    rm geckodriver-$GECKODRIVER_VERSION-linux64.tar.gz
