# Ansible Podman

This is an Ansible playbook that provide a quick installation of Podman and Nvidia Toolkit.

## Installaion Dependencies

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
podman run --rm --device nvidia.com/gpu=all nvidia/cuda:11.0.3-base-ubuntu20.04 nvidia-smi
```

## Reference

- https://podman-desktop.io/docs/podman/gpu
