# Ansible Role: Helm

This role installs k8s cli utilities [Helm](https://helm.sh) and Kubectl 


## Requirements

N/A

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

Specify whether to install `helm`, `kubectl` or both

```yml
install_helm: true
install_kubectl: true
```
Specify OS and architecture
```yml
k8s_platform: linux
k8s_arch: amd64
```
Specify helm/kubectl versions to be installed
```yml
helm_version: 'v3.2.1'
kubectl_version: "1.21.2"
```

Controls for the version of Helm and Kubectl to be installed. See [available Helm releases](https://github.com/helm/helm/releases/) and [stable kubectl release](https://dl.k8s.io/release/stable.txt)
You can upgrade or downgrade versions by changing the `helm_version` and `kubectl_version`.

```yml
    helm_bin_path: /usr/local/bin/helm
    kubectl_bin_path: /usr/local/bin/kubectl
```

The location where the helm/kubectl binary will be installed.

## Dependencies

None.

## Example Playbook

    - hosts: all
      roles:
        - role: ricsanfre.k8s_cli

## License

MIT / BSD

## Author Information

This role was created by Ricardo Sanchez