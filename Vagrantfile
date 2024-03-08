# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure("2") do |config|
    config.vm.define :servidor do |servidor|
        servidor.vm.box = "bento/ubuntu-23.04-arm64"
        servidor.vm.network :forwarded_port, guest: 5555, host: 5555 
        servidor.vm.network :private_network, ip: "192.168.50.3"
        servidor.vm.hostname = "servidor"
        servidor.vm.synced_folder "/Users/pablito/Telecomunicaciones/sincronizado", "/home/vagrant/sincronizado"
    end

    config.vm.define :cliente do |cliente|
        cliente.vm.box = "bento/ubuntu-23.04-arm64"
        cliente.vm.network :forwarded_port, guest: 5555, host: 5556
        cliente.vm.network :private_network, ip: "192.168.50.2"
        cliente.vm.hostname = "cliente"
    end
end

