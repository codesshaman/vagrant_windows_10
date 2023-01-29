# -*- mode: ruby -*-
# vi: set ft=ruby :

IP =  "192.168.58.93"   # Don't change!
CPU_CORES_COUNT = "4"   # Cnahge if necessary
MEMORY_COUNT = "4096"   # Cnahge if necessary

Vagrant.configure("2") do |win|
    win.vm.box = "senglin/win-10-enterprise-vs2015community"
    win.vm.synced_folder ".", "/vagrant", disabled: true
    win.vm.network :private_network, ip: IP
    win.vm.provider "virtualbox" do |vb|
        vb.name = "windows 10"
        vb.memory = MEMORY_COUNT
        vb.cpus = CPU_CORES_COUNT
        vb.gui = true
    end
  end