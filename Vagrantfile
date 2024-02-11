# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/focal64"
  config.vm.hostname = "nginx"
  config.vm.network "private_network", ip: "192.168.1.55"
  config.vm.provider "virtualbox" do |vb|
    vb.name = "prism9x"
    vb.memory = "1024"
    vb.cpus = "2"
  end

  # Install Nginx
  config.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get -y upgrade
    sudo apt -y install nginx
  SHELL
end