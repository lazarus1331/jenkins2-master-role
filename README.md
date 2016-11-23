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
Defaults:
~~~~~~~~~
env: dev
domain: local.net

jenkins_user_name: jenkins
jenkins_user_group: "{{ jenkins_user_name }}"
jenkins_config_java_options: '-Djava.awt.headless=true -Djenkins.install.runSetupWizard=false'
jenkins_config_listen_address: 127.0.0.1
jenkins_config_port: 8080
jenkins_config_args: "--httpListenAddress={{ jenkins_config_listen_address }} --httpPort={{ jenkins_config_port }} "
jenkins_package_repository: https://pkg.jenkins.io/debian-stable/binary/
jenkins_version: 2.19.3
jenkins_package_url: "{{ jenkins_package_repository }}jenkins_{{ jenkins_version }}_all.deb"

terraform_url: https://releases.hashicorp.com/terraform/0.7.11/terraform_0.7.11_linux_amd64.zip
packer_url: https://releases.hashicorp.com/packer/0.12.0/packer_0.12.0_linux_amd64.zip

jenkins_plugins:
  - github
  - thinbackup
  - ...

python_build_depends:
  - ansible==2.1.1.0
  - Jinja2
  - ...


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

