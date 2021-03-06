# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.

VAGRANTFILE_API_VERSION = "2"
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  	config.vm.define "fubuntuone", primary: true do |fubuntuone|

		fubuntuone.vm.box = "ubuntu/xenial64"
  		fubuntuone.vm.hostname ="fubuntuone"
		fubuntuone.vm.network :public_network, ip: "192.168.1.15"
		fubuntuone.vm.network "forwarded_port", guest: 9001, host: 9001,
    			auto_correct: true
		fubuntuone.vm.network "forwarded_port", guest: 8000, host: 9007,
    			auto_correct: true
  		fubuntuone.vm.network "forwarded_port", guest: 8080, host: 9002,
    			auto_correct: true  
  		fubuntuone.vm.network "forwarded_port", guest: 4004, host: 9003,
    			auto_correct: true
  		fubuntuone.vm.network "forwarded_port", guest: 4001, host: 9004,
    			auto_correct: true
  		fubuntuone.vm.network "forwarded_port", guest: 5001, host: 5001,
    			auto_correct: true
  		fubuntuone.vm.network "forwarded_port", guest: 9006, host: 9006,
    			auto_correct: true
  		
		#BIchain DB ports 
		fubuntuone.vm.network "forwarded_port", guest: 58080, host: 58080,
    			auto_correct: true
  		fubuntuone.vm.network "forwarded_port", guest: 59984, host: 59984,
    			auto_correct: true

		#fubuntuone.vm.provision :shell, :privileged => false, :path => "bootstrap_ubuntu.sh"
		fubuntuone.vm.provider :virtualbox do |vb|
			vb.gui = false # change to `true` if you get "Error: Connection timeout." while booting
			vb.memory = 2048 # warning: this is higher than what our production server has
			vb.cpus = 2
			vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
			vb.customize ["modifyvm", :id, "--natdnsproxy1", "on"]
		end

	end
  	
	config.vm.define "fubuntutwo", primary: true do |fubuntutwo|

		fubuntutwo.vm.box = "ubuntu/xenial64"
  		fubuntutwo.vm.hostname ="fubuntutwo"
		fubuntutwo.vm.network :public_network, ip: "192.168.1.16"
		fubuntuone.vm.network "forwarded_port", guest: 9001, host: 9010,
    			auto_correct: true
		fubuntuone.vm.network "forwarded_port", guest: 9001, host: 9001,
    			auto_correct: true
		fubuntutwo.vm.network "forwarded_port", guest: 8000, host: 9011,
    			auto_correct: true
  		fubuntutwo.vm.network "forwarded_port", guest: 8080, host: 9012,
    			auto_correct: true  
  		fubuntutwo.vm.network "forwarded_port", guest: 4004, host: 9013,
    			auto_correct: true
  		fubuntutwo.vm.network "forwarded_port", guest: 4001, host: 9014,
    			auto_correct: true
  		fubuntutwo.vm.network "forwarded_port", guest: 5001, host: 9015,
    			auto_correct: true
  		fubuntutwo.vm.network "forwarded_port", guest: 9006, host: 9016,
    			auto_correct: true
  		
		#BIchain DB ports 
		fubuntutwo.vm.network "forwarded_port", guest: 58080, host: 48080,
    			auto_correct: true
  		fubuntutwo.vm.network "forwarded_port", guest: 59984, host: 49984,
    			auto_correct: true

		#fubuntuone.vm.provision :shell, :privileged => false, :path => "bootstrap_ubuntu.sh"
		fubuntutwo.vm.provider :virtualbox do |vb|
			vb.gui = false # change to `true` if you get "Error: Connection timeout." while booting
			vb.memory = 2048 # warning: this is higher than what our production server has
			vb.cpus = 2
			vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
			vb.customize ["modifyvm", :id, "--natdnsproxy1", "on"]
		end

	end
	
	config.vm.define "fubuntuthree", primary: true do |fubuntuthree|

		fubuntuthree.vm.box = "ubuntu/xenial64"
  		fubuntuthree.vm.hostname ="fubuntuthree"
		fubuntuthree.vm.network :public_network , ip: "192.168.1.17"
		fubuntuthree.vm.network "forwarded_port", guest: 8000, host: 9021,
    			auto_correct: true
  		fubuntuthree.vm.network "forwarded_port", guest: 8080, host: 9022,
    			auto_correct: true  
  		fubuntuthree.vm.network "forwarded_port", guest: 4004, host: 9023,
    			auto_correct: true
  		fubuntuthree.vm.network "forwarded_port", guest: 4001, host: 9024,
    			auto_correct: true
  		fubuntuthree.vm.network "forwarded_port", guest: 5001, host: 9025,
    			auto_correct: true
  		fubuntuthree.vm.network "forwarded_port", guest: 9006, host: 9026,
    			auto_correct: true
  		fubuntuthree.vm.network "forwarded_port", guest: 9001, host: 9027,
    			auto_correct: true
  		
		#BIchain DB ports 
		fubuntuthree.vm.network "forwarded_port", guest: 58080, host: 38080,
    			auto_correct: true
  		fubuntuthree.vm.network "forwarded_port", guest: 59984, host: 39984,
    			auto_correct: true

		#fubuntuone.vm.provision :shell, :privileged => false, :path => "bootstrap_ubuntu.sh"
		fubuntuthree.vm.provider :virtualbox do |vb|
			vb.gui = false # change to `true` if you get "Error: Connection timeout." while booting
			vb.memory = 2048 # warning: this is higher than what our production server has
			vb.cpus = 2
			vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
			vb.customize ["modifyvm", :id, "--natdnsproxy1", "on"]
		end

	end
	
	
	


  	config.vm.define "fclientone", autostart: false do |fclientone|

		fclientone.vm.box = "alpine/alpine64"
  		fclientone.vm.hostname ="fclientone"
  		fclientone.vm.network "forwarded_port", guest: 8000, host: 9021,
    			auto_correct: true
  		fclientone.vm.network "forwarded_port", guest: 8080, host: 9022,
    			auto_correct: true  
  		fclientone.vm.network "forwarded_port", guest: 4004, host: 9023,
    			auto_correct: true
  		fclientone.vm.network "forwarded_port", guest: 4001, host: 9024,
    			auto_correct: true
  		fclientone.vm.network "forwarded_port", guest: 5001, host: 9025,
    			auto_correct: true
  		fclientone.vm.network "forwarded_port", guest: 9006, host: 9026,
    			auto_correct: true

	end

end
