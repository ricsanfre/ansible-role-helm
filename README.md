# Ansible Role: Helm

This role installs k8s cli utilities [Helm](https://helm.sh) and Kubectl 


## Requirements

N/A

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

```yml
    helm_version: 'v3.2.1'
    helm_platform: linux
    helm_arch: amd64
```

Controls for the version of Helm to be installed. See [available Helm releases](https://github.com/helm/helm/releases/). You can upgrade or downgrade versions by changing the `helm_version`.

```yml
    helm_bin_path: /usr/local/bin/helm
```

The location where the Helm binary will be installed.

## Dependencies

None.

## Example Playbook

    - hosts: all
      roles:
        - role: ricsanfre.helm

## License

MIT / BSD

## Author Information

This role was created by Ricardo Sanchez