# Ansible-server-management
An ansible repository with some of my scripts for various uses for myself but others can make use of as well.


## Applications, services, tools used on endpoints:
The tools I deploy on the endpoints might not be preferred by yourself. But to make it clear, here is what I use. You may need to alter the playbooks for your own use.
- iptables and ipset geoIP blocking
- Apache2
- Docker
- [Pterodactyl (For updating only as of now.)](https://github.com/pterodactyl/panel)
- [OnlyOffice Document Server (Community Edition)](https://github.com/ONLYOFFICE/CommunityServer)
- [Privatebin](https://github.com/PrivateBin/PrivateBin)




## Using this repository

### Ansible:
To use this repository one must be familiar using [Ansible](https://docs.ansible.com/#get_started). Ansible is open-source technology that can perform virtually any IT task and remove complexity from workflows. Instead of having to do work by hand one simply writes so called 'Playbooks' that perform tasks simply based on declarative input.

To run Ansible your system must be running Linux or any Unix-like destribution. Using Windows? Then you'll have to set up WSL first. After you've have an operating system that is eligable for using Ansible on ready then you can run the commands below.


### Setting up virtual environment and installing required modules:
Simply run:
```
python3 -m venv .venv
. .venv/bin/activate
pip install -r requirements.txt
```


### Getting remote hosts ready to use Ansible:
Put the public key of your SSH key file(s) in the 'authorized_keys' file on thje remote host.

Then simply put the hostname and keyfile location in the 'hosts.yaml' file. You can copy and change the contents of the example file.


### Running an Ansible playbook:
From then, you can run the playbooks by using the command:
```
ansible-playbook -i hosts.yaml ./playbooks/<FILE>
```


## Notes on using a secrets file:
The secrets.yaml file needs to be populated by the user in question to with data they require and prefer to use. The basic reason behind using this file this way is to moreso keep sensitive stuff private usable in a simple way without much need for secure vaults or other methods given the usecase for myself is way too small to justify such complexity.
