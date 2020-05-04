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
    - airprint-gcp
```

To get credentials for the Google Cloud Print, the playbook will instruct you to ssh to the server and create an OAuth token for GCP. Rerun the playbook to restart the Google Cloud Print daemon afterward.
Also you will be using the CUPS admin interface to setup your printers - You will be handed a URL for that.
