# -*- mode: ruby -*-
# vi: set ft=ruby sts=2 sw=2 :

Vagrant.configure("2") do |config|
  config.vm.box = "bento/centos-7.3"

  # config.vm.network "forwarded_port", guest: 80, host: 8080
  # config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"
  # config.vm.network "private_network", ip: "192.168.33.10"

  # Create a public network, which generally matched to bridged network.
  # Bridged networks make the machine appear as another physical device on
  # your network.
  # config.vm.network "public_network"

  # Share an additional folder to the guest VM. The first argument is
  # the path on the host to the actual folder. The second argument is
  # the path on the guest to mount the folder. And the optional third
  # argument is a set of non-required options.
  # config.vm.synced_folder "../data", "/vagrant_data"

  config.vm.provision "ansible" do |ansible|
#    ansible.galaxy_role_file = "requirements.yml"
    ansible.playbook = "vagrant-playbook.yml"
  end
end

