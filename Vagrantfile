# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  
  
  config.vm.box = "ubuntu/jammy64"

  # ====================================================
  # 1.Ansible Control Node (Manager Server)
  # ====================================================
  config.vm.define "ansible-control" do |control|
    control.vm.hostname = "ansible-control"
    
    # Host-Only Network setup 
    control.vm.network "private_network", ip: "192.168.56.10"
    
    control.vm.provider "virtualbox" do |vb|
      vb.name = "Ansible-Control-Node"
      vb.memory = "2048" 
      vb.cpus = 2
    end
  end

  # ====================================================
  # 2.Target Web Node 1 (Managed Server 1)
  # ====================================================
  config.vm.define "web-node1" do |node1|
    node1.vm.hostname = "web-node1"
    node1.vm.network "private_network", ip: "192.168.56.11"
    
    node1.vm.provider "virtualbox" do |vb|
      vb.name = "Web-Node-01"
      vb.memory = "1024" # 
      vb.cpus = 1
    end
  end

  # ====================================================
  # 3.Target Web Node 2 (Managed Server 2)
  # ====================================================
  config.vm.define "web-node2" do |node2|
    node2.vm.hostname = "web-node2"
    node2.vm.network "private_network", ip: "192.168.56.12"
    
    node2.vm.provider "virtualbox" do |vb|
      vb.name = "Web-Node-02"
      vb.memory = "1024" 
      vb.cpus = 1
    end
  end

end
