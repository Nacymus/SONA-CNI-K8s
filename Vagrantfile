# -*- mode: ruby -*-
# vi: set ft=ruby :

ENV['VAGRANT_DEFAULT_PROVIDER'] = 'virtualbox'

Vagrant.configure("2") do |config|
  config.vm.provider "virtualbox" do |v|
        v.memory = 2048
        v.cpus = 2
  end
  config.vm.define "K8s-master" do |config|
  config.vm.hostname = "K8s-master"
  config.vm.network "private_network", ip: "10.168.1.11"
  config.vm.box = "generic/centos7"
  config.vm.post_up_message = "VM 1 Ok"
  end

  config.vm.define "K8s-worker1" do |config|
  config.vm.hostname = "K8s-worker1"
  config.vm.network "private_network", ip: "10.168.2.12"
  config.vm.box = "generic/centos7"
  config.vm.post_up_message = "VM 2 Ok"
  end

  config.vm.define "K8s-worker2" do |config|
  config.vm.hostname = "K8S-worker2"
  config.vm.network "private_network", ip: "10.168.3.13"
  config.vm.box = "generic/centos7"
  config.vm.post_up_message = "VM 3 Ok"
  end
end
