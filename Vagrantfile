# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant::Config.run do |config|
  config.vm.box = "ubuntu-12.04-x64"

  config.vm.provision :chef_solo do |chef|
    chef.cookbooks_path = "cookbooks"
    chef.add_recipe "ruby_build"
    chef.add_recipe "rbenv::system"
    chef.add_recipe "rbenv::vagrant"
    chef.add_recipe "apt"
    chef.add_recipe "chefenv"
    chef.add_recipe "shimizukawa-env"

    # You may also specify custom JSON attributes:
    chef.json = {
      "rbenv" => {
        "rubies" => ["1.9.3-p392"],
        "global" => "1.9.3-p392",
        "gems" => {
          "1.9.3-p392" => [{"name" => "bundler"}]
        },
        "user_installs" => [
          {"user" => "vagrant"}
        ]
      },
      :chefenv => {
        :user => 'vagrant',
        :copyright => 'Takayuki SHIMIZUKAWA',
        :email => 'shimizukawa@gmail.com',
      },
    }
  end
end
