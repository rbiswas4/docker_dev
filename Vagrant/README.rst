I was able to install vagrant and virtualbox on OSX Mavericks using homebrew and cask. I needed to put in the root password to do the installation.

# For some reason I had trouble with the following brew cask installs of virtual
# box, vagrant and vagrant manager. I tried the first two, the download of the 
# dmg would work, but then the process stalled.
# Finally I got rid of my current brew-cask
brew unlink brew-cask
# Then installed brew-cask 
brew install caskroom/cask/brew-cask
# Redid instructions to install vagrant, virtual-box, vagrant-manager
brew cask install vagrant
brew cask install virtualbox
brew cask install vagrant-manager

# Work in the directory Vagrant
mkdir Vagrant
cd Vagrant/
# Start a publicly available box
vagrant init hashicorp/precise32
vagrant up # This spun up the image in virtalbox
vagrant ssh # log into the VM
# I was able to touch /vagrant/foo which wrote to my OSX directory Vagrant 
# where the VM was launched from.
# I was able to write Hello_world programs in python and C,
# compile and execute the c code. However, there was no C++
# compiler. 
# Used `sudo apt-get install g++` to get g++, after which I 
# could compile and execute the C++ program.
# This shows that it connects to the internet
# Further, I was able to ssh to another machine, but stopped as I did not have ssh_keys, (If we are sharing VMs, how do people use ssh-keys?).
# `exit` returns to OSX host, can see the machine in VirtualBox 
# `vagrant destroy` apparently destroys the image (have not tried)
# `vagrant share` apparently shares the image publicly (have not tried)

