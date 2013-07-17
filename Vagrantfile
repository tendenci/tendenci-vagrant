# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
    config.vm.box = "tendenci-precise64"
    config.vm.box_url = "http://tendenci-virtual-appliances.s3.amazonaws.com/tendenci-precise64-vagrant.box"

    config.vm.network :forwarded_port, guest: 8080, host: 8080  # nginx

    config.vm.hostname = "tendenci"
    config.vm.synced_folder "themes", "/var/www/tendencisite/themes"
    config.vm.synced_folder "addons", "/var/www/tendencisite/addons"

    config.vm.provider :virtualbox do |vb|
        vb.customize ["modifyvm", :id, "--memory", 512]
    end

end