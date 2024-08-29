# Tailscale Docker Sidecar Configuration Examples

This repository provides examples of using [Tailscale](https://tailscale.com/) in a sidecar configuration within Docker, specifically for integrating Tailscale with services like [AdGuard Home](https://github.com/AdguardTeam/AdGuardHome), [Plex Media Server](https://www.plex.tv/) and [Beszel Monitoring](https://github.com/henrygd/beszel). By leveraging Tailscale's secure networking capabilities, these examples demonstrate how to seamlessly route traffic through Tailscale while maintaining service functionality and security.

The provided configurations showcase how to set up Tailscale alongside Docker services, with a focus on ensuring connectivity, security, and ease of deployment. The examples include configurations for Tailscale authentication, state management, and service routing.

The example below illustrates a basic setup where Tailscale is used to manage network traffic for AdGuard Home in a Docker environment, utilizing a sidecar approach to simplify networking and enhance security.

## Currently Available Example Configurations

- [AdGuard Home](adguardhome)
- [Beszel](beszel)
- [Plex](plex)

## Documentation

- [Tailscale.com - Knowledge Base](https://tailscale.com/kb)
- [Tailscale.com - Docker Tailscale Guide](https://tailscale.com/blog/docker-tailscale-guide)

## License

[MIT](https://choosealicense.com/licenses/mit/)
