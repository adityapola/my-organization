# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.

config.vm.provision "chef_solo" do |chef|
  chef.cookbooks_path = "../chef/cookbooks"
  chef.add_recipe "tomcat::default"
  chef.run-list  = [ "recipe[tomcat::default]" ]
end
Vagrant.configure(2) do |config|

  config.vm.box = "hashicorp/precise64"

config.vm.synced_folder "/Users/polaaditya/Documents/project/", "/var/www"

config.vm.provider "virtualbox" do |vb|  
 vb.memory = "1024"
 end


end
