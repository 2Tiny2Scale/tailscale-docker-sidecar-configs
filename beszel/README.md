# Beszel with Tailscale Sidecar Configuration

This Docker Compose configuration integrates [Beszel](https://github.com/henrygd/beszel) with Tailscale in a sidecar setup to enhance secure communication over a private Tailscale network. By utilizing Tailscale, this configuration ensures that all communication handled by Beszel remains secure and private within your Tailscale network.

## Beszel

[Beszel](https://github.com/henrygd/beszel) is a lightweight, open-source communication tool designed for secure messaging and real-time collaboration. It provides an encrypted and efficient way to exchange messages and share information within teams or between devices. This configuration leverages Beszel in conjunction with Tailscale to ensure that all messages are securely transmitted over a private, encrypted network.

### Hub

The [Hub](hub) is the core component of Beszel, responsible for routing messages between agents and managing the overall communication flow. In this configuration, the Beszel Hub runs in its own Docker service and is secured by the Tailscale sidecar, ensuring that all traffic to and from the Hub is encrypted and restricted to your Tailscale network.

### Agent

The [Agent](agent) is the client-side component that connects to the Hub to send and receive messages. Multiple agents can connect to a single Hub, enabling secure communication across different devices. The Agent also benefits from the Tailscale sidecar, ensuring that its communication with the Hub is conducted over a secure, private network.

## Configuration Overview

In this setup, the `tailscale-beszel` service runs Tailscale, which manages secure networking for the Beszel service. The `beszel` service connects to the Tailscale network stack using Docker's `network_mode: service:` configuration. This setup guarantees that Beszel's communication channels are only accessible through the Tailscale network, providing an extra layer of security and privacy.
