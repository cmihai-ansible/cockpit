Role Name
=========

cockpit

[![Build Status](https://travis-ci.org/cmihai-ansible/cockpit.svg?branch=master)](https://travis-ci.org/cmihai-ansible/cockpit)

Requirements
------------

- For RHEL, a Red Hat subscription or functional local repository.

Role Variables
--------------


Dependencies
------------

- For Red Hat, subscription-manager.

Example Playbook
----------------

    - hosts: servers
      roles:
         - role: cockpit

    - name: set tuned state
      import_role:
        name: cockpit
      vars:
        cockpit_remove_packages: true
        cockpit_enable_service: true
        cockpit_firewall_configure: true
        cockpit_firewall_rules:
          - service: service_name
      tags: cockpit

License
-------

MIT

Author Information
------------------

- [Mihai Criveti](https://www.linkedin.com/in/crivetimihai/)
