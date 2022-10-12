# exec playbook
```sh
ansible-playbook playbooks/09-gather-facts-validation.yaml > facts
```
# on browser console create variable
```console
var ansible_facts = json from ansible.builtin.debug var 'ansible_facts'
```
# access data
```console
ansible_facts.all_ipv4_addresses
['172.31.83.85']

ansible_facts.fqdn
'ip-172-31-83-85.ec2.internal'

...etc
```
