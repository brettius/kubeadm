# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|
    # The most common configuration options are documented and commented below.
    # For a complete reference, please see the online documentation at
    # https://docs.vagrantup.com.

    # Every Vagrant development environment requires a box. You can search for
    # boxes at https://atlas.hashicorp.com/search.

    # Docker EE node for ubuntu 16.04
    config.vm.define "master" do |master|
      master.vm.box = "ubuntu/xenial64"
      master.vm.network "private_network", ip: "172.28.128.34"
      master.landrush.tld = 'local'
      master.vm.hostname = "master.local"
      master.landrush.enabled = true
      config.vm.provider :virtualbox do |vb|
        vb.customize ["modifyvm", :id, "--memory", "8196"]
        vb.customize ["modifyvm", :id, "--cpus", "4"]
      end
    end

    # Docker EE node for ubuntu 16.04
    config.vm.define "worker1" do |worker1|
      worker1.vm.box = "ubuntu/xenial64"
      worker1.vm.network "private_network", ip: "172.28.128.35"
      worker1.landrush.tld = 'local'
      worker1.vm.hostname = "worker1.local"
      worker1.landrush.enabled = true
      config.vm.provider :virtualbox do |vb|
        vb.customize ["modifyvm", :id, "--memory", "4096"]
        vb.customize ["modifyvm", :id, "--cpus", "2"]
      end
    end

    # Docker EE DTR node for ubuntu 16.04
    config.vm.define "worker2" do |worker2|
      worker2.vm.box = "ubuntu/xenial64"
      worker2.vm.network "private_network", ip: "172.28.128.36"
      worker2.landrush.tld = 'local'
      worker2.vm.hostname = "worker2.local"
      worker2.landrush.enabled = true
      config.vm.provider :virtualbox do |vb|
        vb.customize ["modifyvm", :id, "--memory", "4096"]
        vb.customize ["modifyvm", :id, "--cpus", "2"]
      end
    end
end
