# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
    config.vm.box = "fedora34"
    config.vm.synced_folder '.', '/vagrant', disabled: true
    config.ssh.insert_key = false
  
    config.vm.provider "virtualbox" do |v|
      v.name = "fedora34-pixie"
      v.memory = 1024
      v.cpus = 1
    end
  
    config.vm.hostname = "fedora34-pixie"
    config.vm.network "public_network", bridge: "eth0", ip: "192.168.60.11"
    #config.vm.network :private_network, ip: "192.168.60.11" # Valid range: 192.168.56.0/21 For pxe switch to public network
  
    config.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbook.yml"
      ansible.become = true
    end
  
  end
