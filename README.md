## Intro:

This is an ansible role that bootstraps a Kubernetes cluster with kubeadm On CentOS 7.
The cluster is integrated with the SONA-CNI which is a Kubernetes networking solution
that allows administration of the Cluster with ONOS.


## Give it a try:

This role is meant to make it possible for everyone who wants to deploy a local Kubernetes cluster with SONA-CNI to do that in a few line commands.

First make sure to have these installed on your local machine:


 Ansible 2.11.4

 Vagrant 2.2.14

 Python3

 VirtualBox

With all these setup, just do:

```
$ git pull https://github.com/Nacymus/SONA-CNI-K8s
$ cd SONA-CNI
$ vagrant up
```


Wait for the three machines to start up. then do:

```
$ ansible-playbook playbook.yml -u vagrant -i K8s-inventory
```


Wait for the playbook to finish executing.

DONE!

