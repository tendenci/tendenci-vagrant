# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
    config.vm.box = "tendenci-vagrant-precise64"
    config.vm.box_url = "http://tendenci-virtual-appliances.s3.amazonaws.com/tendenci-vagrant-precise64.box"

    config.vm.network :forwarded_port, guest: 8080, host: 8080  # nginx

    config.vm.hostname = "tendenci"
    config.vm.synced_folder "themes", "/var/www/tendencisite/themes"
    config.vm.synced_folder "addons", "/var/www/tendencisite/addons"

    # For Developers, sync local copy of Tendenci package
    # Uncomment the line below and change the first path
    # to match your local clone of tendenci for development
    # config.vm.synced_folder "/path/to/your/clone/of/tendenci", "/var/www/tendencisite/venv/lib/python2.7/site-packages/tendenci"

    config.vm.provider :virtualbox do |vb|
        vb.customize ["modifyvm", :id, "--memory", 512]
    end

end
