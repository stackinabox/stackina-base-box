####  Stackina-base-box

This project is intended to be used with Vagrant and VirtualBox.  It gives you a vagrant base box with OpenStack (DevStack) pre-installed and configured to run with Ubuntu's nova-lxd hypervisor driver.  

##### Getting Started
  -  Download & install GIT for your platform  
  -  Clone this repo to your system
    ````git clone https://github.com/tpouyer/stackina-base-box.git````  
  -  Change into the newly cloned 'stackina-base-box' directory
  -  Now change into the 'vagrant' directory
  -  Copy the `Personalization.dict` in the same directory with the name `Personalization`
  -  Note if you have a problem with nfs shares (or you are running on windows) open the newly
     copied `Personalization` file and change the `$use_nfs = true` property to `$use_nfs = false` 
  -  Change back into the `stackina-base-box/vagrant` folder and exectue vagrant:
     `vagrant up --provider=virtualbox`  
  -  Wait for the vagrant process to fully boot the virtual machine
  -  If you don't have vagrant and virtualbox already installed change to the `stackina-base-box/scripts/install-vagrant` folder and run the following command for your system:  
     `./install-vagrant-linux-ubuntu.sh`  

###### Access the box

  -  Horizon Web Console:  
     `http://192.168.27.100`  
     `username: demo`  
     `password: labstack`  

     `username: admin`  
     `password: labstack`  

  -  Virtual Machine  
     From the stackina-base-box/vagrant folder run the following command:  
     `vagrant ssh`

     You can also simply ssh into the box using the following command:  
     `ssh vagrant@192.168.27.100`

  -  If you are running this base box on Windows and you don't have access to a shell.  Open you web browser to the following url to get access to a shell for this virtual machine from a web console:  
    `http://192.168.27.100:4200`
    `username: vagrant`
    `password: vagrant`
    