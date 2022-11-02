# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
    config.vm.box = "debian11"
    config.vm.synced_folder '.', '/vagrant', disabled: true
    config.ssh.insert_key = false
  
    config.vm.provider "virtualbox" do |v|
      v.name = "debian-pixie"
      v.memory = 1024
      v.cpus = 1
    end
  
    config.vm.hostname = "debian-pixie"
    config.vm.network :private_network, ip: "192.168.60.11" # Valid range: 192.168.56.0/21
  
    config.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbook.yml"
      ansible.become = true
    end
  
  end