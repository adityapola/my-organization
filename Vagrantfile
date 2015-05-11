# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure(2) do |config|

  config.vm.box = "hashicorp/precise64"

  config.vm.network "private_network", ip: "192.168.33.10"
  config.berkshelf.enabled = true
  config.berkshelf.berksfile_path = 'chef/cookbooks/task_tomcat/Berksfile'
  config.vm.provision :chef_zero do |chef|
    chef.cookbooks_path = "chef/cookbooks"
    chef.roles_path = "chef/roles"
    chef.add_role "tomcat_sample"
  end
   
end
