# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.define "centos" do |centos7|
    centos7.vm.box  = "geerlingguy/centos7"
    centos7.vm.hostname = "centos"
    centos7.vm.network :private_network, ip: "192.168.2.200"
    centos7.vm.provider "virtualbox" do |v|
      v.memory = "1024"
      v.cpus = "1"
    end
  end

  config.vm.define "debian" do |debian|
    debian.vm.box = "mokote/debian9"
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
