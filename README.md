# Ansible For GEM

This repository is my testing ground for ansible. The objective is to create an ansible playbook that will load necessary software from a control host onto a CTP7 or GLIB.

## Instructions

Make sure that you are logged into the control host and that it has ansible installed.

### Connecting to CTP7s/GLIBs

First, write the name of the CTP7/GLIB in `ansible_hosts` and make sure that the control host has access to the CTP7/GLIB. Then, try pinging the CTP7/GLIB with the gemuser.

```bash
ansible all -u gemuser -i ansible_hosts -m ping
```


