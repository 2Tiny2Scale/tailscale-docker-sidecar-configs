# Tailscale Exit Node Configuration

This Docker Compose configuration sets up a Tailscale Exit Node, allowing devices in your Tailscale network to route their internet traffic securely through this node. By configuring a Tailscale Exit Node, you can enhance the privacy and security of your internet browsing by routing traffic through a trusted network, such as your home or office, rather than relying on potentially less secure public networks.

## Tailscale Exit Node

A Tailscale Exit Node is a device within your Tailscale network that other devices can use as a gateway to the internet. By setting up an Exit Node, you ensure that all traffic from connected devices is routed through a secure and private network, benefiting from the encryption and privacy that Tailscale provides. This configuration leverages Docker to easily deploy and manage a Tailscale Exit Node, offering a straightforward solution to secure your internet traffic.

## Configuration Overview

In this setup, the `tailscale` service runs a Tailscale container configured as an Exit Node. The key configurations include:

- **TS_AUTHKEY**: This environment variable is where you insert your Tailscale authentication key.
- **TS_EXTRA_ARGS**: The `--advertise-exit-node` flag is used to designate this container as an Exit Node within your Tailscale network.
- **Sysctls**: The system controls `net.ipv4.ip_forward` and `net.ipv6.conf.all.forwarding` are enabled to allow IP forwarding, which is necessary for routing traffic through the Exit Node.
- **Network Mode**: The `bridge` network mode is used to create a virtual network interface for the container, enabling it to handle traffic routing.

This configuration ensures that the Tailscale Exit Node is set up correctly, allowing devices connected to your Tailscale network to securely route their internet traffic through this node.
