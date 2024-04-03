# -*- mode: ruby -*-
#vi: set ft=ruby:

vagrant.configure ("2") do |config|
    #Configuration for master-node -Ubuntu/20.04 VM
    config.vm.define "master" do |master|
        master.vm.box = "ubuntu/focal64"
        master.vm.hostname = "master-node"
        master.vm.network "private_network", type: "dhcp"
        master.vm.network "forwarded_port", guest: 80, host: 8080
    end

    #Configuration for slave-node -CentOS/7 VM 
    config.vm.define "centos" do |centos|
        centos.vm.box = "centos/7"
        centos.vm.hostname = "centos-slave"
        centos.vm.network "private_network", type: "dhcp"
        centos.vm.network "forwarded_port", guest: 80, host: 8081
    end

    #Configuration for slave-node -Debian/10 VM
    config.vm.define "debian" do |debian|
        debian.vm.box = "debian/buster64"
        debian.vm.hostname = "debian-slave"
        debian.vm.network "private_network", type: "dhcp"
        debian.vm.network "forwarded_port", guest: 80, host: 8082
    end

end
