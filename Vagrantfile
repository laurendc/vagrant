# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.define "centos" do |centos|
    centos.vm.box  = "geerlingguy/centos7"
    centos.vm.hostname = "centos"
    centos.vm.network :private_network, ip: "192.168.2.200"
    centos.vm.provider "virtualbox" do |v|
      v.memory = "1024"
      v.cpus = "1"
    end
    centos.vm.provision "ansible" do |ansible|
      ansible.playbook = "ansible/centos.yml"
      ansible.verbose = "vvv"
      ansible.become = true
    end
  end

  config.vm.define "debian" do |debian|
    debian.vm.box = "debian/stretch64"
    debian.vm.hostname = "debian"
    debian.vm.network :private_network, ip: "192.168.2.201"
    debian.vm.provider "virtualbox" do |v|
      v.memory = "1024"
      v.cpus = "1"
    end
    debian.vm.provision "ansible" do |ansible|
      ansible.playbook = "ansible/debian.yml"
      ansible.verbose = "vvv"
    end
  end
end
