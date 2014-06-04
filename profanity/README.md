# profanity - XMPP client

Runs [profanity](http://www.profanity.im/) within a tmux session over ssh.

## Installation

    docker build . -t "akoenig/profanity"

## Run

    docker run -d -t -p 127.0.0.1:8023:22 akoenig/profanity

## Connect

    ssh root@localhost -p 8023

## Author

Copyright 2014, [André König](http://andrekoenig.info) (andre.koenig@posteo.de)
