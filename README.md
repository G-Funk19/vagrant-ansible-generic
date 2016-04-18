Vagrant
=======
Vagrant is a tool for building and distributing development environments.

Vagrant version used: 1.8.1

For further information visit their website: https://www.vagrantup.com/docs/

Ansible
=======
Ansible is an IT automation tool. It can configure systems, deploy software, and orchestrate more advanced IT task such as continuous deployments.

Ansible version used: 1.9.4

For more information visit their website: http://docs.ansible.com/ansible/intro_getting_started.html

Quick Start
===========

 * Simple setup way to have a distributed environments for testing your apps and your software components
 * Manage virtual machines quickly and in parallel 
 * No need root access

Vagrantfile
===========

 * Configured with specific vagrant box: centos-7
 * 6 virtual machines: 1 haproxy - 2 apache web server - 2 tomcat application server - 1 postgresql server
 * Each machine used 1 vCPU and 1024Mo for RAM memory
 * Private network which enable communication between virtual machines

Authors
=========

 * Ansible was created by [Michael DeHaan]
 * Vagrant was create by [Mitchell Hashimoto]