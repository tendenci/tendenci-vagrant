# Tendenci Vagrant

A Vagrant setup file and initial addons and themes directories for launching a virtualbox using vagrant.

To use, please install Vagrant (http://www.vagrantup.com/) and Virtualbox (https://www.virtualbox.org/wiki/Downloads) first.

Next, clone this repo and cd into the new tendenci-vagrant folder.

To launch the virtualbox, run `vagrant up`. The **first** run will download the box (700+ mb), so it may take a few minutes. Once download, subsequent uses of `vagrant up` can be run in under a minute.

This will start a server. Travel to http://127.0.0.1:8080 in your browser to use the Tendenci site. You can use `admin` as the username and password to the Tendenci site at http://127.0.0.1:8080/login/.

To edit themes or add a new theme, please see the files in the tendenci-vagrant/themes folder.
