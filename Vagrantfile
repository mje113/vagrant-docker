# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box     = 'raring'
  config.vm.box_url = 'http://cloud-images.ubuntu.com/raring/current/raring-server-cloudimg-vagrant-amd64-disk1.box'
  config.vm.provision :shell, path: 'bootstrap'

  config.vm.network   :forwarded_port, guest: 8091,  host: 8091
  config.vm.network   :forwarded_port, guest: 8092,  host: 8092
  config.vm.network   :forwarded_port, guest: 11211, host: 11211
  config.vm.network   :forwarded_port, guest: 11210, host: 11210

  config.vm.provider :virtualbox do |vb|
    vb.customize ['modifyvm', :id, '--memory', '1024']
  end

end
