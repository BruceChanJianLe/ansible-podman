# Ansible Podman

This is an Ansible playbook that provide a quick installation of Podman and Nvidia Toolkit.

## Package Dependencies

```bash
sudo apt install ansible git -y
```
## Installation

```bash
ansible-pull -U https://github.com/brucechanjianle/ansible-podman -K
```

## Verification

```bash
podman run hello-world
```

With NVIDIA Container Toolkit.
```bash
podman run --rm --device nvidia.com/gpu=all nvidia/cuda:11.0.3-base-ubuntu20.04 nvidia-smi
```

## Reference

- https://kresna.dev/solving-podman-error-short-name-did-not-resolve-to-an-alias-and-no-unqualified-search-registries/
- https://podman-desktop.io/docs/podman/gpu
