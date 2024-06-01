# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"  # Usaremos Ubuntu 18.04 como base
  config.vm.network "private_network", ip: "192.168.56.10"  # Configuración de red
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "2048"  # Asignación de RAM
    vb.cpus = 2  # Asignación de núcleos de CPU
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
  end
end
