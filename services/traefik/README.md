# Node-RED with Tailscale Sidecar Configuration

This Docker Compose configuration sets up [Traefik](https://traefik.io/) with Tailscale as a sidecar container ......

## SERVICE

[Traefik](https://traefik.io/) is a leading modern open source reverse proxy and ingress controller that makes deploying services and APIs easy. Traefik integrates with your existing infrastructure components and configures itself automatically and dynamically.

#### Simplified Operation, Complex Deployments
Traefik is designed to be as simple as possible to operate, but capable of handling large, highly-complex deployments across a wide range of environments and protocols in public, private, and hybrid clouds.

#### Enhanced with Powerful Middleware Suite
Traefik also comes with a powerful set of middlewares that enhance its capabilities to include load balancing, API gateway, orchestrator ingress, and more.

#### Introductory Videos
You can find high level and deep dive videos on [videos.traefik.io](https://videos.traefik.io)

## Configuration Overview

In this setup, the `tailscale-traefik` service runs Tailscale, which manages secure networking for the SERVICE. The `traefik` service utilizes the Tailscale network stack via Docker's `network_mode: tailscale:` configuration. This setup ensures that SERVICE's service is only accessible through the Tailscale network (or locally, if preferred), providing an extra layer of security and privacy for your SERVICE.

## Files to check

Please check the following contents for validity as some variables need to be defined upfront.

- `.env` // This files hold the main parts
- `./config/serve.json` // PreConfigured
