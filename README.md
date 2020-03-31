# dnsmasq-cloudflare-doh-chinalist-arm
A dockerfile for building a dnsmasq container with DoH and China Domain List.

Support raspberrypi.

# Usage
``` bash
mkdir docker-chinalist-dns && cd docker-chinalist-dns
git clone https://github.com/ZHLHZHU/dnsmasq-cloudflare-doh-chinalist-arm.git .
docker build -t chinalist-dns:latest . --network host
sudo docker run -p 53:53/tcp -p 53:53/udp --restart=always --name="mydns" -d chinalist-dns:latest
```
