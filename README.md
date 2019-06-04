# Ansible main repository

From this point you can apply all playbooks in this project.
Below you can find information how to proceed with it.

TODO:
- all necessary installations should be performed from ansible automatically (gcloud, helm, kubect, ...)
- all necessary credentials should be automatically applied in env (GCP vs K8S authorization on Jenkins host)

### If you want to configure terraform environment

* install python3.7
* install pipenv software (```https://pypi.org/project/pipenv/```)
* install ansible (>= 2.8) (```https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html``` - propobly you have to use ```pip``` instalation method)

### If you want to apply playbooks

Be sure (within ```hosts``` file) that all hosts are defined properly (IP addresses, names, groups) and then apply below command (use your proper user account for hosts ssh connections):
```
$ ansible-playbook -u root project.yml
```

### If you want to use new role

You have to update ```requirements.yml``` file (please don't use "latest" tag for role version) and then apply below command:
```
$ ansible-galaxy install -r requirements.yml -p roles
```
