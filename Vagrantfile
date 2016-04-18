# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # Configure Virtual Box
  #config.ssh.private_key_path = "~/.ssh/id_rsa"
  #config.ssh.insert_key = false
  config.ssh.forward_agent = true
  config.vm.box = "centos-7"
  config.vm.box_check_update = false
  config.vm.provider "virtualbox" do |v|
    v.memory = 1024
    v.cpus = 1
  end

  # Configure HAProxy load balancer
#  config.vm.define "haproxy" do |haproxy|
#    haproxy.vm.network "private_network", ip: "192.168.1.10", virtualbox__intnet: true
#    haproxy.vm.provision "ansible" do |ansible|
#    ansible.playbook = "ansible/ha-playbook.yml"
#    ansible.groups = {
#      "LB" => ["haproxy"]
#    }
#    end
#  end
#
#  # Configure Apache 1
#  config.vm.define "apache1" do |apache1|
#    apache1.vm.network "private_network", ip: "192.168.1.20", virtualbox__intnet: true
#    apache1.vm.provision "ansible" do |ansible|
#      ansible.playbook = "ansible/apache-playbook.yml"
#      ansible.groups = {
#        "FRONT" => ["apache1"]
#      }
#    end
#  end
#  # Configure Apache 2
#  config.vm.define "apache2" do |apache2|
#    apache2.vm.network "private_network", ip: "192.168.1.21", virtualbox__intnet: true
#    apache2.vm.provision "ansible" do |ansible|
#      ansible.playbook = "ansible/apache-playbook.yml"
#      ansible.groups = {
#        "FRONT" => ["apache2"]
#      }
#    end
#  end

  # Configure Apache 2
  config.vm.define "tomcat1" do |tomcat1|
    tomcat1.vm.network "private_network", ip: "192.168.1.30", virtualbox__intnet: true
    tomcat1.vm.provision "ansible" do |ansible|
      ansible.playbook = "ansible/tomcat-playbook.yml"
      ansible.groups = {
        "BACK" => ["tomcat1"]
      }
    end
  end

  # Configure Apache tomcat 2
  config.vm.define "tomcat2" do |tomcat2|
    tomcat2.vm.network "private_network", ip: "192.168.1.31", virtualbox__intnet: true
    tomcat2.vm.provision "ansible" do |ansible|
      ansible.playbook = "ansible/tomcat-playbook.yml"
      ansible.groups = {
        "BACK" => ["tomcat2"]
      }
    end
  end

#  # Configure PostgreSQL server
#  config.vm.define "postgres" do |postgres|
#    postgres.vm.network "private_network", ip: "192.168.1.40", virtualbox__intnet: true
#  end
end