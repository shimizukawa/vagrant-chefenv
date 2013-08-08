# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu-12.04-x64"
  config.vm.box_url = "http://files.vagrantup.com/precise64.box"
  config.vm.hostname = "chefenv"

  config.vm.provision :chef_solo do |chef|
    #chef.log_level = 'debug'
    chef.cookbooks_path = "cookbooks"
    chef.roles_path = "roles"
    chef.add_role "chefenv"
    chef.add_recipe "shimizukawa-env"

    # You may also specify custom JSON attributes:
    chef.json = {
      :chefenv => {
        :user => 'vagrant',
        :copyright => 'Takayuki SHIMIZUKAWA',
        :email => 'shimizukawa@gmail.com',
      },
    }
  end
end
