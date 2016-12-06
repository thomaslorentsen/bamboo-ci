# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "centos/7"
  config.vm.network "private_network", ip: "192.168.33.135"

  config.vm.provision :ansible do |ansible|
    # Disable default limit to connect to all the machines
    ansible.playbook = 'ansible/playbook.yml'
    ansible.inventory_path = 'ansible/inventories/hosts.ini'
    ansible.limit = 'all'
  end
end
