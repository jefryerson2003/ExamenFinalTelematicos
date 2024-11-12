<<<<<<< HEAD
Vagrant.configure("2") do |config|
  config.vm.define :servidorMonitor do |servidorMonitor|
    servidorMonitor.vm.box = "bento/ubuntu-22.04"
    servidorMonitor.vm.network :private_network, ip: "192.168.60.3"
    servidorMonitor.vm.provider "virtualbox" do |vb|
      vb.memory = "1024"
      vb.cpus = 2
    end
    servidorMonitor.vm.provision "shell", inline: <<-SHELL
      # Actualizar repositorios
      sudo apt-get update -y

      # Instalar wget y curl si no están disponibles
      sudo apt-get install -y wget curl
    SHELL
=======
# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.define :servidorWeb do |servidorWeb|
    servidorWeb.vm.box = "bento/ubuntu-22.04"
    servidorWeb.vm.network :private_network, ip: "192.168.60.3"
    servidorWeb.vm.provision "file", source: "webapp", destination: "/home/vagrant/webapp"
    servidorWeb.vm.provision "file", source: "init.sql", destination: "/home/vagrant/init.sql"
    servidorWeb.vm.provision "shell", path: "script.sh"
    servidorWeb.vm.hostname = "servidorWeb"
  end
  config.vm.define :prometheus do |prometheus|
    prometheus.vm.box = "bento/ubuntu-22.04"
    prometheus.vm.network :private_network, ip: "192.168.60.4"
    prometheus.vm.hostname = "prometheus"
>>>>>>> 4fc0e140f632b0a6dfbe4e00f9c2728daa7d1a36
  end
end
