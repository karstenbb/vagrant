# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure("2") do |config|
  
  config.vm.box = "ubuntu/trusty64"
  config.vm.hostname = "tomcat8"

 
   config.vm.network "forwarded_port", guest: 8080, host: 8080
config.vm.provision "shell", path: "provision-tomcat.sh"
  
  # config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"

  


   config.vm.provider "virtualbox" do |vb|
    vb.name = "TomcatDev"
    vb.memory = "1024"
    vb.cpus = 2
  end
end
  #
  # View the documentation for the provider you are using for more
  # information on available options.

  # Enable provisioning with a shell script. Additional provisioners such as
  # Ansible, Chef, Docker, Puppet and Salt are also available. Please see the
  # documentation for more information about their specific syntax and use.
  # config.vm.provision "shell", inline: <<-SHELL
  #   apt-get update
  #   apt-get install -y apache2
  # SHELL

