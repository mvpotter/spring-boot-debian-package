# -*- mode: ruby -*-
# vi: set ft=ruby :

$script = <<SCRIPT
sudo add-apt-repository ppa:webupd8team/java
sudo apt-get update
sudo dpkg -i /vagrant/deb/target/gs-spring-boot.deb
echo oracle-java8-installer shared/accepted-oracle-license-v1-1 select true | sudo /usr/bin/debconf-set-selections
sudo apt-get -fqy install
SCRIPT

Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/trusty64"
  config.vm.network "private_network", ip: "65.0.0.20"
  config.vm.provision "shell", inline: $script

end
