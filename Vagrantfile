# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
    config.vm.box = "ubuntu/trusty64"
    config.vm.hostname = "keepbench"

    config.vm.provider "virtualbox" do |vbx|
        vbx.name = "keepbench"
        vbx.memory = 4096
        vbx.cpus = 2
    end

    config.vm.provision "ansible" do |ansible|
        ansible.playbook = "provision.yml"
    end
end
