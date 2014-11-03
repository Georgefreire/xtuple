### Vagrant Virtual Machine ###

The xTuple server can be quickly set up on a platform of your choice using a Vagrant Virtual Machine:

Need to update an existing xTuple setup? Skip to [here](#update-an-existing-xtuple-virtual-machine).

#### Install VirtualBox and Vagrant ####

* Download and install [VirtualBox 4.3.12](https://www.virtualbox.org/wiki/downloads).
  * Do not open VirtualBox or create a virtual machine. This will be handled by Vagrant.
* Download and install [Vagrant 1.6.4](http://www.vagrantup.com/download-archive/v1.6.4.html).
  * Use the Vagrant download page. Package managers like apt-get and gem install will install an older version of Vagrant.
  * This installation requires a reboot before any Vagrant commands can be performed

#### Create the xTuple Server ####

*The following commands should run in a command prompt on your host computer.*   [ [HOW?] ](https://github.com/xtuple/xtuple-vagrant/wiki/Vagrant-Tips-and-Tricks#using-a-command-prompt)

* Navigate to a directory of your choosing, or use these commands to create a new directory:

         mkdir xtuple-vagrant
         cd xtuple-vagrant

* Inside of that directory, create a Vagrant configuration file, called a Vagrantfile:
  * You may be able to copy this file directly to your computer with the following command:
        
           curl "https://raw.githubusercontent.com/xtuple/xtuple-
           vagrant/master/demo/Vagrantfile" -o "Vagrantfile"

  * Or else you can create an empty text file called "Vagrantfile" (no .txt or other extension) and paste in the [content](https://raw.githubusercontent.com/xtuple/xtuple-vagrant/master/demo/Vagrantfile).

* Once you have a Vagrantfile in the directory, you create and start the xTuple server with the following command:

        vagrant up

* After the vagrant box has finished loading, log into it with the following command:

        vagrant ssh

* Once logged into the vagrant box, go back to the [Quickstart](https://github.com/xtuple/xtuple-server/wiki/0.-Quickstart) page and follow the instructions there.

#### Update an existing xTuple Virtual Machine ####

If you need to upgrade, use these commands to update an existing setup:

    vagrant destroy
    vagrant box update
    vagrant up