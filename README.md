# Ansible Kubernetes Installation

This Ansible playbook automates the installation of a Kubernetes cluster on Ubuntu-based systems. It supports both master and worker nodes.

## Features

- Disables swap and cleans `/etc/fstab`
- Replaces DNS with internal servers
- Installs container runtime (containerd)
- Sets up Docker and Kubernetes repositories
- Installs Kubernetes components (kubeadm, kubelet, kubectl)
- Configures containerd with systemd cgroups
- Enables kernel modules and IP forwarding
- Reboots the nodes after installation

## Usage

1. Update your Ansible inventory with `masters` and `workers` groups.
2. Run the playbook:

```bash
ansible-playbook -i inventory.ini k8s-install.yml
```

## Requirements

- Ubuntu 18.04 or newer
- Ansible 2.9+
