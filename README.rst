====================
jenkins-master-role
====================

Ansible role to manage Jenkins master

* License: Apache License, Version 2.0

Description
-----------

Requirements
------------

Packages
~~~~~~~~

Package repository index files should be up to date before using this role, we
do not manage them.

Role Variables
--------------

Dependencies
------------

Example Playbook
----------------

.. code-block:: yaml

    - name: Install jenkins
      hosts: jenkins
      roles:
        - ansible-role-jenkins

Based Upon
----------
Source: https://git.openstack.org/cgit/openstack/ansible-role-jenkins

