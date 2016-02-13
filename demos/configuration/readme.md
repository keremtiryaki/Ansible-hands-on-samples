
# Ansible configuration settings order of operations
1 $ANSIBLE_CONFIG 	- Env variable
2 ./ansible.cfg 	- you can use this configuration files with git
3 ~/.ansible.cfg 	- home settings you need to set the conf for all team members
4 /etc/ansible.cfg  - global config


Attention: Not merged. Fisrt one wins!

To use overriding we need combile 1 and 2 together

For example we have an ansbile.cfg file in the current directory.
```
[defaults]
host_key_checking=False
```


We need to set an Env variable to override it
```
export ANSIBLE_HOST_KEY_CHECKING=True
echo $ANSIBLE_HOST_KEY_CHECKING
```

to be continued!

# Ansible Modules
Doc command

```
ansible-doc -l
ansible-doc -s
ansible-doc <name>

```