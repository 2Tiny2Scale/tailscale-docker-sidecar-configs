# Node-RED with Tailscale Sidecar Configuration

This Docker Compose configuration sets up [Node-RED](https://nodered.org/) with Tailscale as a sidecar container ......

## SERVICE

[Node-RED](https://nodered.org/) is a programming tool for wiring together hardware devices, APIs and online services in new and interesting ways.
It provides a browser-based editor that makes it easy to wire together flows using the wide range of nodes in the palette that can be deployed to its runtime in a single-click.

## Configuration Overview

In this setup, the `tailscale-SERVICE` service runs Tailscale, which manages secure networking for the SERVICE. The `SERVICE` service utilizes the Tailscale network stack via Docker's `network_mode: service:` configuration. This setup ensures that SERVICE's service is only accessible through the Tailscale network (or locally, if preferred), providing an extra layer of security and privacy for your SERVICE.

## Files to check

Please check the following contents for validity as some variables need to be defined upfront.

- `.env` // This files hold the main parts
- `./config/serve.json` // PreConfigured
