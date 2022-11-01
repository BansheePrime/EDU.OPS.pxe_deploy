# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
    config.vm.box = "-- name for vagrant box" # use Debian 11
    config.vm.synced_folder '.', '/vagrant', disabled: true # probably not
    config.ssh.insert_key = false # ignore ssh for now
  
    config.vm.provider "virtualbox" do |v|
      v.name = "debian_pixie"
      v.memory = 1024
      v.cpus = 1
    end
  
    config.vm.hostname = "debian_pixie"
    config.vm.network :private_network, ip: "192.168.10.11" # 192.168.10.0/24
  
    config.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbooks/main.yml"
      ansible.become = true
    end
  
  end