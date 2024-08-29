# AdGuard Home with Tailscale Sidecar Configuration

This Docker Compose configuration sets up [AdGuard Home](https://github.com/AdguardTeam/AdGuardHome) with Tailscale as a sidecar container to securely route DNS traffic over a private Tailscale network. By using Tailscale in a sidecar configuration, you can enhance the security and privacy of your DNS queries, ensuring that they are only accessible within your Tailscale network.

## AdGuard Home

[AdGuard Home](https://github.com/AdguardTeam/AdGuardHome) is a network-wide software that blocks ads and trackers. It provides a powerful DNS filtering solution that can protect all devices on your network. This configuration allows AdGuard Home to be used in combination with Tailscale, providing a secure and private network for DNS queries.

## Configuration Overview

In this setup, the `tailscale-adguardhome` service runs Tailscale, which manages secure networking for the AdGuard Home service. The `adguardhome` service uses the Tailscale network stack via Docker's `network_mode: service:` configuration. This setup ensures that AdGuard Home's DNS service is only accessible through the Tailscale network (or local as well, if preferred).
