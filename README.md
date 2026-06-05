Ansible Deployment Scripts
==========================

Ansible based deployment scripts for deploying the current state of HA-STS.

Steps to Run
------------

1. Setup and deploy each of the nodes.
   * Install operating systems on nodes.
   * Setup ansible user on the node. ???
   * Setup DHCP / Static IPs for nodes.
   * Setup DNS References / Entries for nodes.
   * Copy SSH Public Key to Authorized Keys file on nodes.

2. Create / Update the `inventory.ini` file with host information.

3. Create a venv to run the project.

4. Run the project.
   * For all nodes: `ansible-playbook --verbose -i inventory.ini playbook.yaml
`
   * For one node: ...


Notes
-----

```
PATH="/usr/pkg/sbin:/usr/pkg/bin:$PATH"
PKG_PATH="https://cdn.NetBSD.org/pub/pkgsrc/packages/NetBSD/aarch64/10.0_2025Q1/All/"
export PATH PKG_PATH
pkg_add -u python313
```


ToDos
-----

* Merge the mosquitto configs
* Make sure the mosquitto configs work for the installation (review settings)
* Make the mosquitto role work for NetBSD (current) and Linux
* Write the steps to run the project in README.md
* Split roles out to own repos, making a better layout of the project.

