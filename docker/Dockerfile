FROM ubuntu:latest

LABEL maintainer=”YourName”

RUN apt-get update && \
    apt-get -qy full-upgrade && \
    apt-get install -qy curl && \
        apt-get install -qy git && \
    curl -sSL https://get.docker.com/ | sh

RUN git clone --depth 1 https://github.com/supabase/supabase
RUN cd supabase/docker
RUN cp .env.example .env
RUN docker compose pull
RUN docker compose up -d
