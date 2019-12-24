Role Name
=========

cockpit

[![Build Status](https://travis-ci.org/cmihai-ansible/cockpit.svg?branch=master)](https://travis-ci.org/cmihai-ansible/cockpit)

Ansible Galaxy:
---------------

[https://galaxy.ansible.com/crivetimihai/cockpit](https://galaxy.ansible.com/crivetimihai/cockpit)

```bash
ansible-galaxy install crivetimihai.cockpit
```

Requirements
------------

- For RHEL, a Red Hat subscription or functional local repository.

Role Variables
--------------

```
cockpit_enable_service: true
cockpit_firewall_configure: true
cockpit_firewall_rules:
  - port: 9090
```

Dependencies
------------

- For Red Hat, subscription-manager.

Example Playbook
----------------

```yaml
---
- name: Install cockpit on localhost
  hosts:
    - localhost
  connection: local

  tasks:
    - name: cockpit is configured
      import_role:
        name: crivetimihai.cockpit
      vars:
        cockpit_remove_packages: true
        cockpit_enable_service: true
        cockpit_firewall_configure: true
        cockpit_firewall_rules:
          - service:
      tags: cockpit
```

License
-------

MIT

Author Information
------------------

- [Mihai Criveti](https://www.linkedin.com/in/crivetimihai/)
