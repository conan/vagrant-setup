# Install Vagrant

You can just install in Windows, Cygwin will understand.  

http://downloads.vagrantup.com/

# Install VirtualBox

https://www.virtualbox.org/wiki/Downloads

# Get a vagrant box

From Cygwin, download a base box to get going:

    vagrant box add precise64 http://files.vagrantup.com/precise64.box
    
# Install vbguest plugin for keeping VirtualBox Guest Additions in sync

    vagrant plugin install vagrant-vbguest

# Vagrantfile

You'll need a [Vagrantfile](https://github.com/conan/vagrant-setup/blob/master/Vagrantfile) to define some boxes.

# Start it up

Fire up a box:

    vagrant up linux

There will be loads of crap in the output about outdated Vagrantfiles and VirtualBox-specific parameters, because vagrant likes to complain.  The shared folder bit will probably fail, saying:

    The following SSH command responded with a non-zero exit status.
    Vagrant assumes that this means the command failed!

    mount -t vboxsf -o uid=`id -u vagrant`,gid=`id -g vagrant` v-root /vagrant

Details here: http://docs-v1.vagrantup.com/v1/docs/troubleshooting.html

Connect to the box:

    vagrant ssh linux

Do some stuff to fix this:

