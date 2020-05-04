# ansible-airprint-gcp

Use this ansible role to setup your local Debian based server for AirPrint and Google Cloud Print.

## Installing

Add a section to `requirements.yaml` like:

```
- name: airprint-gcp
  src: https://github.com/hilli/ansible-airprint-gcp.git
```

and then fetch your external roles with:

```
ansible-galaxy install -r requirements.yaml
```

## Using
Add the role to your playbook:

```
---
- name: AirPrint on the server
  hosts: server
  become: yes

  roles:
    - role: airprint-gcp
```
