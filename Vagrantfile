# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.define "centos7" do |centos7|
    config.vm.box  = "geerlingguy/centos7"
    config.vm.provider "virtualbox" do |v|
      v.memory = "1024"
      v.cpus = "1"
    end
  end

  config.vm.define "debian-stetch" do |debian|
    config.vm.box = "mokote/debian9"
    config.vm.provider "virtualbox" do |v|
      v.memory = "1024"
      v.cpus = "1"
    end
  end
end
