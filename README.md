# Ansible main repository

From this point you can apply all playbooks in this project.
Below you can find information how to proceed with it.

### If you want to just apply playbooks

Be sure (within ```hosts``` file) that all hosts are defined properly (IP addresses, names, groups) and then apply below command:
```
$ ansible-playbook -u root project.yml
```

### If you want to use new role

You have to update ```requirements.yml``` file (please don't use "latest" tag for definitions) and then apply below command:
```
$ ansible-galaxy install -r requirements.yml
```


