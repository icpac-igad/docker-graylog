# Graylog Docker Compose files

## Introduction

Quickly spin up a [Graylog](https://docs.graylog.org/) instance.

## Prerequisites
- [Docker](https://docs.docker.com/engine/install/)
- [Docker-Compose](https://docs.docker.com/compose/install/)

## Configure Graylog

All the [Graylog configurations](https://docs.graylog.org/docs/server-conf) can be set via environment variables. Just prefix the parameter name with `GRAYLOG_` and put it in upper case.

There is an environment file (`.env.sample`) where you can store these environment variables. Rename this to `.env` so docker-compose will pick it up.

      cp .env.sample .env


**Important:** Be sure to to set the `GRAYLOG_PASSWORD_SECRET` and `GRAYLOG_ROOT_PASSWORD_SHA2` environment variables in the .env file! Graylog won't start without these.

## Starting Graylog

After you've configured `GRAYLOG_PASSWORD_SECRET` and `GRAYLOG_ROOT_PASSWORD_SHA2`, run these commands to start the instance:

    docker-compose up

To start it daemonized, run:

    docker-compose up -d
