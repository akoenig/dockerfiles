FROM zefhemel/sshd

MAINTAINER André König <andre.koenig@posteo.de>

RUN apt-get update && apt-get install -y git build-essential wget automake autoconf

RUN git clone https://github.com/strophe/libstrophe

WORKDIR libstrophe
RUN ./bootstrap.sh && ./configure && make && make install

RUN wget https://github.com/boothj5/profanity/archive/0.4.2.tar.gz && tar xvfz 0.4.2.tar.gz

WORKDIR /profanity-0.4.2

RUN ./configure && make && make install
