# alafia-caddy

## Description

Alafia-specific deployment of [caddy](https://caddyserver.com/) based on [a modified Docker image](https://github.com/lucaslorentz/caddy-docker-proxy). This app is mostly hidden from the user. It contains essentially just a systemd service file that is required for other applications. Caddy provides a server that maps alafia apps run in the browser to *.alafia domain names.

## Usage

Meant to be used as a submodule in [alafia-apps](https://github.com/Alafia-Ai/alafia-apps).

`Makefile` can be manually invoked with the following options:

- `make` or `make build`: Locally build the Docker image
- `make install`: Install the files in the `deploy/` directory, and if relevant, install systemd service files and modify `/etc/hosts/`
- `make uninstall`: Removes all installed files, and if relevant, removes systemd services and resets `/etc/hosts/` 
