# Simplekyc mid-level Tecnical test Ansible configuration

This file explains the purpose of the Ansible attached to the main repository for the Simple KYC mid-level technical test. See more information about Ansible on (https://en.wikipedia.org/wiki/Ansible_(software)).


# Objective

The purpose of this Ansible is to provide the installation and configuration of the necessary COTS for the Simple KYC mid-level test as mentioned before. This Ansible will be executed on two Ubuntu VMs, as requested.

# 1. Ansible structure

This Ansible presents the following structure:

1. "php.yaml" playbook to be applied.
2. "monitoring.yaml" playbook to be applied.
3. "inventories" with the hosts where Ansible is executed

# 2. Environment

This Ansible must be executed only in the machines included in the inventories. Each machine has a different configuration in particular, so different tasks are executed depending on the desired host. KYC-VM1 contains the PHP configuration where KYC-VM2 contains the monitoring (Grafana/Prometheus) setup. The standard user is "kyc_ops" and to access the machines you need the private key, given apart from this repository.

Machine public and private IPs are the following:


[PUBLIC IPs]
```
KYC-VM1: 20.77.2.169
KYC-VM2: 20.39.225.116
```

[PRIVATE IPs]
```
KYC-VM1: 10.0.0.4
KYC-VM2: 10.0.0.6
```

# 3. Requirements

To be able to launch and configure Ansible, you need a machine as an Ansible control node, see the requirements in the official installation guide: (https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html).

# 4. Ansible launch

Once Ansible has been configured properly, it can be launched. For that purpose, execute the Ansible from your host ansible node the following command:

```
$> cd <Ansible root path>
$> ansible-playbook -u kyc_ops --private-key <path/to/private-key.pem> <playbook to be executed>
```