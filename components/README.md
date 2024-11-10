## Components

This path contains Kustomize components that can be added to overlays based upon preference. The example "dev" overlay is very opinionated about which services it supports but this allows the repo to be modularized for other implementations. For example, swapping Plex for Emby or Jellyfin. This allows maintainers to supply different components based upon provided support without having to couple the services tightly to the deployment.

It also allows disabling of certain unwanted services if desired, such as request managers or subtitle managers.

### Development

To add a component, create a new folder like you would for any Kustomization overlay. But use a [Component object](https://github.com/kubernetes-sigs/kustomize/blob/master/examples/components.md) instead. Avoid component interdependencies. Add it to the `dev` overlay.