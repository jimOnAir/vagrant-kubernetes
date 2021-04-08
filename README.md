# Vagrant Docker Swarm cluster setup

Automatic Kubernetes cluster setup with Vagrant and Ansible

## Running

Just run:

```console
$ vagrant up
```

and wait for setup to complete

## Hosts

- `k8s-master` - kubernetes master
- `k8s-worker-1`, etc... - kubernetes workers

## Configuration

Vagrant file contains following constants:

- `IMAGE_NAME = "ubuntu/focal64"` - Vagrant box image. `"ubuntu/focal64"` - the only one is supported
- `SLAVE_COUNT = 2` - Workers count
- `SUBNET_BASE = "192.168.200."` - Private subnet address
- `MASTER_IP = SUBNET_BASE + "2"` - `k8s-master` ip address
