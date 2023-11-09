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

This will provide a shell in the virtual machine via ssh. The default username and password is `vagrant`.
