# DNS Security && VPN
## Install
Download Repository
```
git clone git@github.com:leespe11/rpi-nginx-website-moniting.git
````
Change the configuration to your requirements: **config.env**
Execute permissions for run script
```
chmod +x run
```
Start the service
```
./run
```
### PiHole & Unbound DNS
More information about these services can be credited here:
--*1. [Pihole](https://hub.docker.com/r/pihole/pihole)
--*1. [klutchell/unbound](https://hub.docker.com/r/klutchell/unbound)

DNSSEC is enabled by default
This Pihole instance supports DNS over HTTPS (DoH) or DNS over TLS (DoT)

The dns service is running on port 53
### Squid & Privoxy
More information about this service can be credited here: [squid-privoxy](https://github.com/synopsis8/squid-privoxy)
To connect to the proxy service use port 3218
```
ip_address:3218
```

