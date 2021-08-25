# PiHole with DNS over HTTPS (DoH)

This Docker compose file uses Traefik 2.x as a http/tcp/udp proxy for PiHole with CloudFlare and LetsEncrypt for on demand SSL certificate generation and domain validation.

## Requirements

* [Docker](https://www.docker.com/)
* [Docker Compose](https://docs.docker.com/compose/install/)*
* [A domain name](https://www.namecheap.com/)
* [A CloudFlare account](https://cloudflare.com/)
* [A Cloudflare API Token](https://go-acme.github.io/lego/dns/cloudflare/#api-tokens)
* [TXT records in CloudFlare](https://www.cloudflare.com/learning/dns/dns-records/dns-txt-record/)

*<sub>If you are using a device with an ARM processor use one of the alternative install options for Docker Compose.</sub>
## Setup

Set values for your environment in the `.env` file. Optionally, set `PASSWORD` and `TIME_ZONE` environment variables for the PiHole container.

Start the containers:

```shell
docker-compose up -d
```

Verify you're using DoH!

https://1.1.1.1/help

![](https://i.imgur.com/RhrpaoH.png)
