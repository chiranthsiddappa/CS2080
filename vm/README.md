# Virtual Machines

## Installation

1. Install [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
1. Install [Vagrant](https://developer.hashicorp.com/vagrant/downloads?product_intent=vagrant)
    * Have VMWare? Install the [VMWare Utility](https://developer.hashicorp.com/vagrant/downloads/vmware)

## Verification

In a terminal, verify the vagrant install with the following:

```sh
~$ vagrant -v
Vagrant 2.4.0
```

## Start the Virtual Machine

```sh
~$ vagrant up
```

## Verify the VM

```sh
~$ vagrant ssh
```

This will provide a shell in the virtual machine via ssh.

## Port Forwarding

To access network services running inside the container, we will need to use port forwarding.

### Setup SSH Config

Be sure to secure the permissions on the config file, otherwise it will be ignored.

```sh
vagrant ssh-config > ssh_config
chmod 600 ssh_config
```

The name of the vagrant box will be the first name in the file called `Host`, usually `default`.

### Forward a Port via SSH

The following will expose the port 80 from inside the vm to a port 8080 as localhost.

```sh
ssh -F ssh_config -L 8080:localhost:80 default
```
