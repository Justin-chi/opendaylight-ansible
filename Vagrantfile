# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # All Vagrant configuration is done here. The most common configuration
  # options are documented and commented below. For a complete reference,
  # please see the online documentation at vagrantup.com.

  # Every Vagrant virtual environment requires a box to build off of.
  config.vm.define "odl-controller" do |controller|
    controller.vm.box ="chef/centos-7.0"

    controller.vm.network "private_network", ip: "10.1.0.15"
    controller.vm.provision "ansible" do |ansible|
      ansible.playbook = "odl-controller.yml"
    end

    controller.vm.provider "virtualbox" do |vbox|
      vbox.memory = 2048
    end

  end


end

