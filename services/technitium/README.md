# Technitium DNS server with Tailscale Sidecar Configuration

This Docker Compose configuration sets up a [Technitium DNS Server](https://github.com/TechnitiumSoftware/DnsServer)) with Tailscale as a sidecar container ......

## Technitium

[Technitium DNS Server](https://github.com/TechnitiumSoftware/DnsServer) information about Technitium...

## Configuration Overview

In this setup, the Technitium Service runs on Tailscale, which manages secure networking for the Technitium DNS Services. The `Technitium` utilizes the Tailscale network stack via Docker's `network_mode: technitium:` configuration. This setup ensures that Technitium's Technitium is only accessible through the Tailscale network (or locally, if preferred. Modifications nescsary), providing an extra layer of security and privacy for your Technitium.

## Files to check

Please check the following contents for validity as some variables need to be defined upfront.

- `.env` // This files hold the main parts (preconfigured)
- `./config/serve.json` // This file contains the service port for tailscale (preconfigured)
