# Portainer integration for Home Assistant

## Forked from the original by [tomaae](https://github.com/tomaae/homeassistant-portainer)

![GitHub release (latest by date)](https://img.shields.io/github/v/release/supleed2/homeassistant-portainer?style=plastic)
[![hacs_badge](https://img.shields.io/badge/HACS-Default-41BDF5.svg?style=plastic)](https://github.com/hacs/integration)
![GitHub all releases](https://img.shields.io/github/downloads/supleed2/homeassistant-portainer/total?style=plastic)

![GitHub commits since latest release](https://img.shields.io/github/commits-since/supleed2/homeassistant-portainer/latest?style=plastic)
![GitHub commit activity](https://img.shields.io/github/commit-activity/m/supleed2/homeassistant-portainer?style=plastic)
![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/supleed2/homeassistant-portainer/ci.yml?style=plastic)

[![Help localize](https://img.shields.io/badge/lokalise-join-green?style=plastic&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAA4AAAAOCAYAAAAfSC3RAAAAGXRFWHRTb2Z0d2FyZQBBZG9iZSBJbWFnZVJlYWR5ccllPAAAAyhpVFh0WE1MOmNvbS5hZG9iZS54bXAAAAAAADw/eHBhY2tldCBiZWdpbj0i77u/IiBpZD0iVzVNME1wQ2VoaUh6cmVTek5UY3prYzlkIj8+IDx4OnhtcG1ldGEgeG1sbnM6eD0iYWRvYmU6bnM6bWV0YS8iIHg6eG1wdGs9IkFkb2JlIFhNUCBDb3JlIDUuNi1jMTQ1IDc5LjE2MzQ5OSwgMjAxOC8wOC8xMy0xNjo0MDoyMiAgICAgICAgIj4gPHJkZjpSREYgeG1sbnM6cmRmPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5LzAyLzIyLXJkZi1zeW50YXgtbnMjIj4gPHJkZjpEZXNjcmlwdGlvbiByZGY6YWJvdXQ9IiIgeG1sbnM6eG1wTU09Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC9tbS8iIHhtbG5zOnN0UmVmPSJodHRwOi8vbnMuYWRvYmUuY29tL3hhcC8xLjAvc1R5cGUvUmVzb3VyY2VSZWYjIiB4bWxuczp4bXA9Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC8iIHhtcE1NOkRvY3VtZW50SUQ9InhtcC5kaWQ6REVCNzgzOEY4NDYxMTFFQUIyMEY4Njc0NzVDOUZFMkMiIHhtcE1NOkluc3RhbmNlSUQ9InhtcC5paWQ6REVCNzgzOEU4NDYxMTFFQUIyMEY4Njc0NzVDOUZFMkMiIHhtcDpDcmVhdG9yVG9vbD0iQWRvYmUgUGhvdG9zaG9wIENDIDIwMTcgKE1hY2ludG9zaCkiPiA8eG1wTU06RGVyaXZlZEZyb20gc3RSZWY6aW5zdGFuY2VJRD0ieG1wLmlpZDozN0ZDRUY4Rjc0M0UxMUU3QUQ2MDg4M0Q0MkE0NjNCNSIgc3RSZWY6ZG9jdW1lbnRJRD0ieG1wLmRpZDozN0ZDRUY5MDc0M0UxMUU3QUQ2MDg4M0Q0MkE0NjNCNSIvPiA8L3JkZjpEZXNjcmlwdGlvbj4gPC9yZGY6UkRGPiA8L3g6eG1wbWV0YT4gPD94cGFja2V0IGVuZD0iciI/Pjs1zyIAAABVSURBVHjaYvz//z8DOYCJgUxAtkYW9+mXyXIrI7l+ZGHc0k5nGxkupdHZxve1yQR1CjbPZURXh9dGoGJZIPUI2QC4JEgjIfyuJuk/uhgj3dMqQIABAPEGTZ/+h0kEAAAAAElFTkSuQmCC)](https://app.lokalise.com/public/892665226456f113e0a814.16864793/) (Upstream localisation)

![Portainer Logo](https://raw.githubusercontent.com/supleed2/homeassistant-portainer/master/docs/assets/images/ui/logo.png)

Monitor and control Portainer from Home Assistant.

Features:

- List Endpoints, and containers per endpoint
- List Containers, and state of container

# Features

## Endpoints

List of portainer endpoint.

![Endpoints](https://raw.githubusercontent.com/supleed2/homeassistant-portainer/master/docs/assets/images/ui/endpoints.png)

## Containers

List of containers.

![Containers](https://raw.githubusercontent.com/supleed2/homeassistant-portainer/master/docs/assets/images/ui/containers.png)

# Install integration

The **upstream** integration is distributed using [HACS](https://hacs.xyz/). You can find it under "Integrations", named "Portainer"

**This** integration can be added as a "Custom repository", via the 3-dot menu in the top-right of HACS. Add the repository URL (`https://github.com/supleed2/homeassistant-portainer`) and select type "Integration".

## Get portainer access token

1. Login into your portainer instance
1. Click you username at top right and select "My Account"
1. Under "Access tokens", click "Add access token"
1. Enter name for your access token (can be anything, for example "homeassistant")
1. Copy displayed access token for use in integration setup

## Setup integration

Setup this integration for your Portainer in Home Assistant via `Configuration -> Integrations -> Add -> Portainer`.
You can add this integration several times for different portainer instances.

- "Name of the integration" - Friendly name for this Portainer instance
- "Host" - Use hostname or IP and port (example: portainer.domain.tld or 192.168.0.2:9000)
- "Access token" - Use access token from previous step
- "Use SSL" - Connect to portainer using SSL
- "Verify SSL certificate" - Validate SSL certificate (must be trusted certificate)

## Configuration

When setup is done, it is possilbe to cunfigure custom attibutes for each entry via `Configuration -> Integrations -> Portainer -> Configure`.

List of supported custom attibutes:

- "Health check" - Checks the container health state and updates the sensor state.
- "Restart policy" - Checks how and when the container restarts after stopping.

![Configuration](https://raw.githubusercontent.com/supleed2/homeassistant-portainer/master/docs/assets/images/ui/options.png)

# Development

## Translation

To help out with the translation you need an account on Lokalise, the easiest way to get one is to [click here](https://lokalise.com/login/) then select "Log in with GitHub". After you have created your account [click here to join Portainer project on Lokalise](https://app.lokalise.com/public/892665226456f113e0a814.16864793/).

If you want to add translations for a language that is not listed please [open a Feature request (on the Upstream repository)](https://github.com/tomaae/homeassistant-portainer/issues/new?labels=enhancement&title=%5BLokalise%5D%20Add%20new%20translations%20language).

## Enabling debug

To enable debug for Portainer integration, add following to your configuration.yaml:
```
logger:
  default: info
  logs:
    custom_components.portainer: debug
```
