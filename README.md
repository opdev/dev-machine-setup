# Development machine setup

This repository contains Ansible roles and playbooks to help setting up a machine (laptop or desktop) with the tools required for operator development.

## Usage

### Prerequisites

- Ansible is installed.
- Access to the network.

### Running the playbooks

1. Edit and customize the playbook `opdev_<os>_setup.yml` which corresponds to your operating system.  Currently MacOS, Fedora Linux and immutable Linux distributions such as Fedora Silverblue are supported.

2. Run `ansible-playbook opdev_<os>_setup.yml` as-is or with overriding the default parameters for each role (see [roles](roles/)).
   
## Development and contribution

- Issues can be opened freely.

- A `Vagrantfile` is included to help contribute to the Fedora flow, even if you are running on a Mac.  Make sure you have Vagrant and virtualization software installed (e.g. Virtualbox) and run `vagrant up`.

- Flows can be run with Ansible's verbose and check flags (`-vvv --check`) to test. Each role also includes a simple test. 
