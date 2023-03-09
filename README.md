# shipping-go

## hello-api
Demo continous delivery pipeline

# Dependencies

- Go version 1.19

# Setup



## Using build packs

Setup for podman

````
ssh-add -k "$HOME/.ssh/podman-machine-default"
podman system connection default podman-machine-default-root


````

Add to .zshrc

````
export DOCKER_HOST="$(podman system connection ls --format="{{.URI}}" | grep root)"
````

### Build

````
pack build hello-api --builder gcr.io/buildpacks/builder:v1

````
