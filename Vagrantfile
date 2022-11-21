# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.define "rocky" do |rocky|
    rocky.vm.box = "bento/rockylinux-9"
    rocky.vm.hostname = "rocky"
    rocky.vm.network :private_network, ip: "192.168.150.10"
  end
end
