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
  end
end
