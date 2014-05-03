Go to vagrant.com and install vagrant

virtual box, if problems, delete C:\Users\Jose\.VirtualBox

restart

Copy the file lincese.lic from the email into the folder where you are going to run cmd

Cmd (elevated)
	vagrant plugin install vagrant-vmware-workstation
	vagrant plugin license vagrant-vmware-workstation license.lic

if the file `Vagrantfile` doesn't exist
	vagrant init chef/ubuntu-14.04

Then
	vagrant up --provider=vmware_workstation
	
Open PhpStorm

Module folders:

/tmp/vagrant-puppet-1/modules-0/
/etc/puppet/modules/ (empty)
/home/vagrant/.puppet/modules (they are installed here)
/usr/share/puppet/modules (empty)
/vagrant/puppet/modules  (librarian-puppet install puts them here)

puppet master --configprint modulepath
puppet config print

puppet module install puppetlabs-apache [--version 0.0.2] (1.0.1 installed in /home/vagrant/.puppet/modules)
puppet module list
puppet module search apache

sudo apt-get install ruby1.9.1-dev gcc

sudo puppet apply /vagrant/puppet/manifests/site.pp --modulepath="/etc/puppet/modules/" --hiera_config /vagrant/hiera.yaml

sudo puppet apply /vagrant/puppet/manifests/site.pp --modulepath="/vagrant/puppet/modules/" --hiera_config /vagrant/hiera.yaml


sudo gem install puppet
