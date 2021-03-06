Vagrant
=======
Vagrant is a tool for building and distributing development environments.

Vagrant version used: 1.8.1

For further information visit their website: https://www.vagrantup.com/docs/

[Vagrant Box] (https://s3-eu-west-1.amazonaws.com/sype/vagrant/centos-7box.tar)

Ansible
=======
Ansible is an IT automation tool. It can configure systems, deploy software, and orchestrate more advanced IT task such as continuous deployments.

Ansible version used: 2.0.0

For more information visit their website: http://docs.ansible.com/ansible/intro_getting_started.html

Quick Start
===========

 * Simple setup way to have a distributed environments for testing your apps and your software components
 * Manage virtual machines quickly and in parallel 
 * No need root access

Design principles
=================

 * Create simply a development environment within less coupling between front-end and back-end
 * 1 HAproxy
 * 2 apache web server as container for JavaScript front-end for example
 * 2 apache tomcat server as container for J2EE back-end
 * 1 postgresql server for your database
 * Enable communication between these machines thanks to vagrant's private network

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
