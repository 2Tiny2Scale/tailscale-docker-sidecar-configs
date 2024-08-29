# Tailscale Docker Sidecar Configuration Examples

This repository provides examples of using [Tailscale](https://tailscale.com/) in a sidecar configuration within Docker, specifically for integrating Tailscale with services like [AdGuard Home](https://github.com/AdguardTeam/AdGuardHome), [Plex Media Server](https://www.plex.tv/) and [Beszel Monitoring](https://github.com/henrygd/beszel). By leveraging Tailscale's secure networking capabilities, these examples demonstrate how to seamlessly route traffic through Tailscale while maintaining service functionality and security.

The provided configurations showcase how to set up Tailscale alongside Docker services, with a focus on ensuring connectivity, security, and ease of deployment. The examples include configurations for Tailscale authentication, state management, and service routing.

The example below illustrates a basic setup where Tailscale is used to manage network traffic for AdGuard Home in a Docker environment, utilizing a sidecar approach to simplify networking and enhance security.

## Currently Available Example Configurations

- [AdGuard Home](adguardhome)
- [Beszel](beszel)
- [NextCloud](nextcloud)
- [Plex](plex)
- [Stirling-PDF](stirlingpdf)
- [Tailscale Exit Node](tailscale-exit-node)
- [uptime-kuma](uptime-kuma)

## Tailscale Funnel vs. Tailscale Serve

In summary, Tailscale Funnel is for securely exposing services to the public internet, while Tailscale Serve is for sharing content within your private Tailscale network. You need to decide how you want to expose your service, the configurations in this repo only expose on the local Tailscale network (Tailnet).

### Tailscale Funnel

Funnel is a feature that allows you to expose services running on your Tailscale network to the public internet securely. It acts as a controlled gateway, enabling external access to specific services without compromising the security of your Tailscale network.

An example configuration for Tailscale Funnel for your service is available [here](funnel-serve/funnel-example.json).

![Tailscale Funnel](images/tailscale-funnel.png)

### Tailscale Serve

Serve is used to host lightweight web services or static content directly on your Tailscale nodes. It allows you to serve HTTP content from your devices to other nodes within your Tailscale network, making it easy to share resources without needing a full web server setup.

An example configuration for Tailscale Serve for your service is available [here](funnel-serve/serve-example.json).

![Tailscale Serve](images/tailscale-serve.png)

## Documentation

- [Tailscale.com - Knowledge Base](https://tailscale.com/kb)
- [Tailscale.com - Funnel](https://tailscale.com/kb/1223/funnel)
- [Tailscale.com - Serve](https://tailscale.com/kb/1242/tailscale-serve)
- [Tailscale.com - Docker Tailscale Guide](https://tailscale.com/blog/docker-tailscale-guide)

## License

[MIT](https://choosealicense.com/licenses/mit/)
