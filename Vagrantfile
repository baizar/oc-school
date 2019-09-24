# -*- mode: ruby -*-
# vi: set ft=ruby :

#VAGRANTFILE_API_VERSION = "2"
Vagrant.require_version ">= 1.7.2"

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version. Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|

  config.vm.define 'master', autostart: false do |el7_2|
    el7_2.vm.box = 'centos/7'
    el7_2.vm.box_check_update = true
    el7_2.vm.network "private_network", ip: "192.168.101.2"
    el7_2.vm.hostname = 'master'
    el7_2.vm.provider "virtualbox" do |vb|
      vb.memory = "2048"
      vb.cpus = 2
    end
  end
 config.vm.define 'compute', autostart: false do |el7_2|
    el7_2.vm.box = 'centos/7'
    el7_2.vm.box_check_update = true
    el7_2.vm.network "private_network", ip: "192.168.101.3"
    el7_2.vm.hostname = 'node1'
    el7_2.vm.provider "virtualbox" do |vb|
      vb.memory = "2048"
      vb.cpus = 2
    end
  end

 config.vm.define 'infra', autostart: false do |el7_2|
    el7_2.vm.box = 'centos/7'
    el7_2.vm.box_check_update = true
    el7_2.vm.network "private_network", ip: "192.168.101.4"
    el7_2.vm.hostname = 'infra-node1'
    el7_2.vm.provider "virtualbox" do |vb|
      vb.memory = "2048"
      vb.cpus = 2
    end
  end

  # uncomment this line if you downloaded the box and want to use it instead
  # config.vm.box = "openshift3"
#  config.vm.synced_folder ".", "/vagrant", disabled:true
#  config.vm.hostname = "origin"


  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine. In the example below,
  # accessing "localhost:8080" will access port 80 on the guest machine.
  # config.vm.network "forwarded_port", guest: 80, host: 8080
  # config.vm.network "forwarded_port", guest: 80, host: 1080
  # config.vm.network "forwarded_port", guest: 443, host: 1443
  # config.vm.network "forwarded_port", guest: 5000, host: 5000
  # config.vm.network "forwarded_port", guest: 8080, host: 8080
  # config.vm.network "forwarded_port", guest: 8443, host: 8443

 # config.vm.provider "virtualbox" do |vb|
     #   vb.gui = true
 #    vb.memory = "6142"
 #    vb.cpus = 2
 #    vb.name = "origin-3.9.0"
 # end

end
