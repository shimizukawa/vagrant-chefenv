chef cookbook maintainance environment by using Vagrant+Chef
=============================================================

requirement
------------

1. vagrant
2. virtualbox

preparation
------------

1. install `virtualbox` by installer.
2. install `vagrant` by installer.
3. `vagrant box add ubuntu-12.04-x86_64 http://dl.dropbox.com/u/1537815/precise64.box`

up environment
---------------

1. `curl -O https://github.com/shimizukawa/vagrant-chef-env/archive/master.zip`
2. `unzip master.zip`
3. `cd vagrant-chef-env-master`
4. `mkdir cookbooks`
5. `cd cookbooks`
6. `curl -O https://github.com/shimizukawa/chef-chefenv/archive/master.zip`
7. `unzip master.zip`
8. `mv chef-chefenv-master chefenv`
9. `cd ..`
10. `vagrant up`

use environment / make cookbook
--------------------------------

1. `vagrant ssh`
2. `knife cookbook create foobar`
