Vagrant.configure("2") do |config|
config.vm.define :cliente do |cliente|
cliente.vm.box = "bento/centos-7.9"
cliente.vm.network :private_network, ip: "192.168.51.2"
cliente.vm.hostname = "cliente"
end

config.vm.define :servidor do |servidor|
servidor.vm.box = "bento/centos-7.9"
servidor.vm.network :private_network, ip: "192.168.51.3"
servidor.vm.network "forwarded_port", guest: 80, host: 4000
servidor.vm.hostname = "servidor"
end

config.vm.define :servidorPXE do |servidor|
servidor.vm.box = "bento/centos-7.9"
servidor.vm.network :private_network, ip: "192.168.1.11"
servidor.vm.hostname = "servidorPXE"

end
end

