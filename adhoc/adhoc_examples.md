# Ansible adhoc commands
```bash
ansible -i inventory ec2 -m ping # module 'ping', using 'inventory' file
ansible ec2 -m ping # module 'ping', using 'ansible.cfg'
ansible oracle -m file -a "path=/tmp/data state=directory" # module 'file', create folder '/tmp/data/'
ansible oracle -m copy -a "src=./.python-version dest=/tmp/data" # module 'copy', copy file
ansible ec2 -m lineinfile -a "path=/home/ansibleuser/prod.env line='SUCK=HUY'" # module 'lineinfile', add new line in file
ansible oracle -m uri -a "url=https://api.github.com/users/dazmagar/repos dest=/home/ansibleuser/dazmagar_repos.json" # module 'uri', send api request
ansible ec2 -m package -a "name=mc state=present" --become # module 'package', will install any package (need sudo privileges)
```
# Ansible inventory adhoc commands
```bash
ansible-inventory -i inventory-multi-files --graph
ansible-inventory -i inventory-group-of-groups --graph
ansible-inventory -i inventory-demo-dynamic/inventory.py --list
ansible-inventory -i inventory-demo-dynamic/inventory.py --host 172.42.42.101
ansible all -i inventory-demo-dynamic/inventory.py -m ping
```
