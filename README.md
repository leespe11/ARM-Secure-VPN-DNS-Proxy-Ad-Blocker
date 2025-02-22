# DNS Security & Wireguard VPN
## Install
Download Repository
```
git clone https://github.com/leespe11/ARM-Secure-VPN-DNS-Proxy-Ad-Blocker.git
````
Change the configuration of **config.env** based on your requirments

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
+ [Pihole](https://hub.docker.com/r/pihole/pihole)
+ [klutchell/unbound](https://hub.docker.com/r/klutchell/unbound)

DNSSEC is enabled by default
This Pihole instance supports DNS over HTTPS (DoH) or DNS over TLS (DoT)

The dns service is running on port **53**

To access the PiHole admin Web interface:
```
http://ip_address/admin
```
### Squid & Privoxy
More information about this service can be credited here: [synopsis8/squid-privoxy](https://github.com/synopsis8/squid-privoxy)

To connect to the proxy service use port **3218**
```
ip_address:3218
```

### Wireguard Vpn
More information about this service can be credited here: [Wireguard](https://hub.docker.com/r/linuxserver/wireguard)

#### Basic Command cheat sheet:
Example in your config.env: 
```
...
PEERS="jhon,mike,adam"
...
```
Show peers one and three QR codes (jhon and adam):
```
docker exec -it wireguard /app/show-peer 1 3
```
Show adam and mike QR codes:
```
docker exec -it wireguard /app/show-peer adman mike
```