# triplea-aws
Ansible playbooks for TripleA servers on AWS

VPC and subnet need to already be setup on AWS. So does the security group.
Currently launches t2.micro EC2 Ubuntu 20 instance (ami-0fb653ca2d3203ac1).


### Requirements
python 3.9+

### Install

```shell
pip install -r requirements.txt
```

### Run

To setup a bot server for the first time.

```shell
ansible-playbook main.yml
```

To update the maps on a bot server.

```shell
ansible-playbook -t update_maps main.yml
```

To deploy a new release of TripleA onto the bot server.

```shell
ansible-playbook --skip-tags update_maps prerelease main.yml
```
