
# ansible-setup-pi 

An Ansible playbook for the basic Raspberry Pi setup. It gathers some roles from Ansible Galaxy to configure:

* users
* networking (including wifi)
* hostname
* keyboard layout
* default locale
* timezone

## Requirements

* Ansible (minimum version 2.2) installed on your local machine
* Raspberry Pi with Raspbian OS
* network access to the Raspberry Pi and sshd enabled
* a user with sudo permissions

## How to run the playbook

Clone this repository.

Copy the the whole directory `env/my_pi` to `env/your_pi` and adapt the Ansible inventory, group and host vars according to your needs. 

Download and install roles from Ansible Galaxy:
```sh
$ ansible-galaxy install -r roles.yml
```
Execute the playbook with your adapted inventory, group and host vars:
```$sh
$ ansible-playbook -i env/your_pi/initial.inventory setup-pi.yml
```
