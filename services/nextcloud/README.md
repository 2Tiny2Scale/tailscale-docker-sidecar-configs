# Nextcloud Server with Tailscale Sidecar Configuration

This Docker Compose configuration sets up [Nextcloud Server](https://github.com/nextcloud/server) with Tailscale as a sidecar container to securely manage and access your personal cloud storage over a private Tailscale network. By using Tailscale in a sidecar configuration, you can enhance the security and privacy of your Nextcloud instance, ensuring that it is only accessible within your Tailscale network.

## Nextcloud Server

[Nextcloud Server](https://github.com/nextcloud/server) is an open-source, self-hosted cloud storage platform that allows you to store, share, and sync your files across multiple devices. It provides a secure and private alternative to commercial cloud services, giving you full control over your data. This configuration leverages Tailscale to securely connect to your Nextcloud instance, protecting your files and personal data from unauthorized access.

## Configuration Overview

In this setup, the `tailscale-nextcloud` service runs Tailscale, which manages secure networking for the Nextcloud Server. The `nextcloud` service uses the Tailscale network stack via Docker's `network_mode: service:` configuration. This setup ensures that Nextcloud's web interface and file synchronization services are only accessible through the Tailscale network (or locally, if preferred), providing an extra layer of security and privacy for your cloud storage solution.
