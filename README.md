# Ansible For GEM

This repository is my testing ground for ansible. The objective is to create an ansible playbook that will load necessary software from a control host onto an AMC (CTP7 or GLIB).

## Instructions

Make sure that you are logged into the control host and that it has ansible installed.

### Connecting to AMCs

First, write the name of the AMCs in `ansible_hosts` and make sure that the control host has access to the AMC. Then, try pinging the AMC with the gemuser.

```bash
ansible all -u gemuser -i ansible_hosts -m ping
```

If this is successful, you should see:

```bash
gem-shelf01-amc01 | SUCCESS => {
    "changed": false, 
    "ping": "pong"
}
```

### Creating the AMC role

To create the AMC role, use the AMC host list.

```bash
ansible-playbook amc.yml -i amc_hosts 
```




