# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.define "kube01" do |kube01|
    kube01.vm.box = "centos/7"
    kube01.vm.hostname = "kube01"
    kube01.vm.network "private_network", ip: "192.168.33.10"
    kube01.vm.provider "virtualbox" do |vb|
      vb.memory = 1536
      vb.cpus = 2
    end
    kube01.vm.provision "shell", inline: <<-SHELL
        sudo yum install -y docker
        sudo usermod -aG dockerroot vagrant
        echo '{ "group": "dockerroot" }' | sudo tee /etc/docker/daemon.json
        sudo systemctl restart docker.service
      SHELL
  end

  config.vm.define "kube02" do |kube02|
    kube02.vm.box = "centos/7"
    kube02.vm.hostname = "kube02"
    kube02.vm.network "private_network", ip: "192.168.33.20"
    kube02.vm.provider "virtualbox" do |vb|
      vb.memory = 1536
      vb.cpus = 2
    end
    kube02.vm.provision "shell", inline: <<-SHELL
        sudo yum install -y docker
        sudo usermod -aG dockerroot vagrant
        echo '{ "group": "dockerroot" }' | sudo tee /etc/docker/daemon.json
        sudo systemctl restart docker.service
      SHELL
  end

  config.vm.define "kube03" do |kube03|
    kube03.vm.box = "centos/7"
    kube03.vm.hostname = "kube03"
    kube03.vm.network "private_network", ip: "192.168.33.30"
    kube03.vm.provider "virtualbox" do |vb|
      vb.memory = 1536
      vb.cpus = 2
    end
    kube03.vm.provision "shell", inline: <<-SHELL
        sudo yum install -y docker
        sudo usermod -aG dockerroot vagrant
        echo '{ "group": "dockerroot" }' | sudo tee /etc/docker/daemon.json
        sudo systemctl restart docker.service
      SHELL
  end
end
