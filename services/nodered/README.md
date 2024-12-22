# Node-RED with Tailscale Sidecar Configuration

This Docker Compose configuration sets up [Node-RED](https://github.com/node-red/node-red) with Tailscale as a sidecar container to securely access and manage your flow-based programming tool over a private Tailscale network. By using Tailscale in a sidecar configuration, you can enhance the security and privacy of your Node-RED instance, ensuring it is only accessible within your Tailscale network.

## Node-RED

[Node-RED](https://github.com/node-red/node-red) is a low-code programming tool for event-driven applications, designed to connect devices, APIs, and online services through an intuitive, browser-based flow editor. It’s widely used for IoT, automation, and integration tasks, offering a powerful yet user-friendly way to build workflows. This configuration leverages Tailscale to securely connect to your Node-RED instance, ensuring that your workflows and configurations are protected from unauthorized access and accessible only via your private Tailscale network.

## Configuration Overview

In this setup, the `tailscale-node-red` service runs Tailscale, which manages secure networking for the Node-RED service. The `node-red` service uses the Tailscale network stack via Docker's `network_mode: service:` configuration. This ensures that Node-RED’s web interface is only accessible through the Tailscale network (or locally, if preferred), providing an additional layer of security and privacy for your flow-based programming environment.
