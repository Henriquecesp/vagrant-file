# Atividade 20/04:
# Subir 3 VM's usando Vagrant, definir redes personalizadas.
# 1 - servidor com CentOS rodando backend   -> Rede IP 172.72.72.10
# 2 - servidor com ubuntu rodando frontend  -> IP 172.72.72.20
# 3 - Windows com Wireshark                 -> IP 172.72.72.30

Vagrant.configure("2") do |config|
  config.vm.provision "shell", inline: "echo Hello"
  config.vm.provider "hyperv"
  config.vm.define "backend" do |backend|
    backend.vm.box = "my-centos"
    backend.vm.network "private_network", ip: "172.72.72.10"
  end

  config.vm.define "frontend" do |frontend|
    frontend.vm.box = "my-ubuntu"
    frontend.vm.network "private_network", ip: "172.72.72.20"
  end

  config.vm.define "wire" do |wire|
    wire.vm.box = "my-windows"
    wire.vm.network "private_network", ip: "172.72.72.30"
  end
end
