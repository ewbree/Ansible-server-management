# Ansible-server-management
An ansible repository with some of my scripts for various uses for myself but others can make use of as well.


## Applications, services, tools used on endpoints:
The tools I deploy on the endpoints might not be preferred by yourself. But to make it clear, here is what I use. You may need to alter the playbooks for your own use.
- Apache2
- Docker
- Pterodactyl (For updating only as of now.)


## Setting up virtual environment to use this repository:
Simply run:
```
python3 -m venv .venv
. .venv/bin/activate
pip install -r requirements.txt
```

From then, you can run the playbooks by using the command:
```
ansible-playbook -i hosts.yaml ./playbooks/<FILE>
```


## Using secrets and hosts file:
The secrets.yaml and hosts.yaml file are mere examples and need to be populated by the user. The basic reason behind using these files this way is to moreso keep sensitive stuff private in a simple way without much need for vaults or other methods given the usecase for myself is way too small.
