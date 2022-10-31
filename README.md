# Initiate microk8s cluster

This project is my learning field for ansible and k8s.
I'm using CentOS VMs installed in my home-network to form a cluster.

## Prerequisites

1. ansible [core 2.13.5]+
2. unix-based servers
3. single login with ssh-key connection to all of the servers

## Usage

1. Edit hosts.yaml - place your k8s servers IPs

2. Run install_microk8s playbook:

```
ansible-playbook install_microk8s.yaml -i ./hosts.yaml
```

3. Run initiate_cluster playbook:

```
ansible-playbook initiate_cluster.yaml -i ./hosts.yaml
```

You can access dashboard under your https://<master node>:10443/, \
the token can be found in /tmp/dashboard_started.txt on master node.
