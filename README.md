# fxsync-docker

This repository is holding a working docker-compose setup for documentation pourpuses
because [syncstorage-rs](https://github.com/mozilla-services/syncstorage-rs)'s documentation
is not very good to explain how to self host the new rust syncserver.

With help of it you can self host the new Firefox sync server, which is written in Rust
and replaces the old python one, which is deprecated.

## Background

`syncstorage-rs` has a [docker release on docker-hub](https://hub.docker.com/r/mozilla/syncstorage-rs/)
but it also needs a database to run, which this docker-compose.yaml helps setting up and connecting.

Theoretically you could run Firefox Account yourself, but for login this project relies on the Mozilla
servers, because setting up and configuring it is quite complex but it does not give much more security.

## Setup

1. Clone this repositoy
2. Copy .env-example into .env (including the dot at the beginning of the file)
3. Put in (random) passwords into .env
4. Put in the domain where you will run your sync server into .env
5. Setup your reverse proxy server (see nginx-example-com.conf)
6. Install the systemd service (see fxsync.service) and enable it

