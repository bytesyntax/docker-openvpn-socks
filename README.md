# Dockerized socks proxy to redirects clients over Open VPN connection

## Setup
The below two files should be added to get it running.
### .env
An .env file in root containing credentials for Open VPN account:
```
OPENVPN_USERNAME=<USERNAME_FOR_OVPN_ACCOUNT>
OPENVPN_PASSWORD=<PASSWORD_FOR_OVPN_ACCOUNT>
OPENVPN_CONFIG_FILE=/etc/openvpn/config.ovpn
SOCKS_PORT=1080
```
### config.ovpn
An config.ovpn file in root containing generated Open VPN config (check with your VPN supplier to generate).
The file will be placed inside the container according to OPENVPN_CONFIG_FILE variable.

## Docker image
See documentation for the Docker image at: https://hub.docker.com/r/jonoh/openvpn-socks (I do not have anything to do with this one so thanks to the author!)
