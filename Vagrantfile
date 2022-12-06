# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "debian/bullseye64"
  config.vm.synced_folder '.', '/vagrant', disabled: true
  config.ssh.insert_key = false

  config.vm.provider "virtualbox" do |vbox|
    vbox.name = "farafmb"
    vbox.memory = 1024
    vbox.cpus = 2
  end

  config.vm.hostname = "farafmb"
  config.vm.network :private_network, ip: "192.168.150.10"

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbooks/main.yaml"
    ansible.become = true
  end
  
end
