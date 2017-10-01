FROM debian:jessie

WORKDIR /usr/src/app

RUN set -ex && \
    apt-get update && \
    apt-get install -y apt-utils supervisor ca-certificates python git build-essential python-dev libxml2-dev libxslt-dev libjpeg-dev librrd-dev rrdtool libffi-dev  && \
    apt-get clean && \
    git clone https://github.com/modoboa/modoboa-installer.git /usr/src/app/ && \
    ./run.py --force localhost

COPY files /

CMD ["supervisord"]
#CMD ["/sbin/init"]
