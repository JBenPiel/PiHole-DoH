# PiHole with DNS over HTTPS (DoH)

This Docker compose file uses Traefik 2.x as a http/tcp/udp proxy for Pihole with CloudFlare and LetsEncrypt for on demand SSL certificate generation and domain validation.

## Requirements

* [Docker](https://www.docker.com/)
* [A domain name](https://www.namecheap.com/)
* [A CloudFlare](https://cloudflare.com/) account with an associated API key
* [TXT records in CloudFlare](https://www.cloudflare.com/learning/dns/dns-records/dns-txt-record/) for validating your domain

## Setup

Replace `email@example.com` with your email address. Set `CF_API_KEY` in the Traefik container environment variables. Replace the various host rules with your domain name. Optionally, set a `PASSWORD` variable for PiHole to be used for login to the dashboard.

Start the containers:

```shell
docker-compose up -d
```

Verify you're using DoH!

https://1.1.1.1/help
