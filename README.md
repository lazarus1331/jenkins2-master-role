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

See Vagrantfile for debian packages to install to support ansible provisioning.

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
        - jenkins2-master-role

Based Upon
----------
Source: https://git.openstack.org/cgit/openstack/ansible-role-jenkins

