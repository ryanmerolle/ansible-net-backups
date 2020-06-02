# ansible-net-backups

## Intro

Example playbook for backing up a wide variety of network device types.  This repo should be helpful for those just getting started with Ansible for Network Devices or those who would like to simplify their previously complex network device backup playbooks that required a different task for each target platform.

In the past, it has been required for users to setup their playbooks with a task per target OS type.  Recently, though not well communicated, Ansible introduced the cli_command and cli_config modules to abstract the common functions for the various network operating systems within one common module.

CLICONF plugin abstracts all the various `<network_os>_config` modules for over [2 dozen network OSes](https://docs.ansible.com/ansible/latest/plugins/cliconf.html).  This plugin is built into the Ansible core fo 2.7.  The backup option was introduced to the [cli_config](https://docs.ansible.com/ansible/modules/cli_config_module.html) module as of Ansible 2.8.

[Ansible Fest 2019: Deep dive with Network connection plugins](https://www.ansible.com/hubfs//AnsibleFest%20ATL%20Slide%20Decks/Deep%20dive%20with%20network%20connection%20plugins%20-%20AnsibleFest%202019.pdf).

## Requirements

This has been tested on and will be supported with the following:

* Ansible: 2.8.x
* Python: 3.6.x - 3.8.x

This is not to say that the playbook will not work as is with older versions of Python (even Python2) or older versions of Ansible (2.7.x+).

## Contributing

Feel free to fork and submit a pull request for any improvements.

## Platform Support

This playbook should support all platforms listed on the [cliconf plugins doc](https://docs.ansible.com/ansible/latest/plugins/cliconf.html).  I cannot test the following platforms currently, but given there is no related config module listed, I suspected the cli_config module may not full be tested/supported with said platform:

* edgeswitch
* eric_eccli
* frr
* netvisor
* routeros
