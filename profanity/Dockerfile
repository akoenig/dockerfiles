FROM zefhemel/sshd

MAINTAINER André König <andre.koenig@posteo.de>

RUN apt-get update && apt-get install -y tmux git build-essential automake autoconf libssl-dev libexpat1-dev libncursesw5-dev libglib2.0-dev libnotify-dev libcurl4-openssl-dev libxss-dev

RUN git clone https://github.com/strophe/libstrophe

WORKDIR /libstrophe
RUN sh ./bootstrap.sh && ./configure && make && make install

WORKDIR /
RUN git clone https://github.com/boothj5/profanity

WORKDIR /profanity
RUN git checkout 0.4.2

RUN ./bootstrap.sh && ./configure && make && make install

ADD bashrc /root/.bashrc
