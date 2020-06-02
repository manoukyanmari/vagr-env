# vagr-env - headless mode to run Virtual Machines

Base OS
bento/ubuntu-16.04 (companyName/version)

VAGR commands
#vagrant init
#vagrant up 
#vagrant destroy
#vagrant reload
#vagrant ssh - exit
#vagrant status
#vagrant global-status
#vagrant halt (name of machine) - shut down

Windows / other OS related

Win:Mkdir "folderName"
#myuser/vagrant.d/boxes/
Sync - config.vm.synced_folder "../data", "/vagrant_data"
config.vm.network "forwarded_port", guest: 80, host: 1234, host_ip: "127.0.0.1"


LINUX GENERAL

LINUX common method - SSH (Cryptographic keys for authentication)
ifconfig - similar to ipconfig 
ls /
"foo" > foo.txt


Providers

vmstat -s  (memory , 1GB default)
vb.memory = "512"
lscpu (cpu allocated)
vb.cpus = 2
lspci -v -s 00:02.0 (show the size- default 8MB)
vb.customize ["modifyvm", :id, "--vram", "16"]


PRovisioners

config.vm.provision "shell", path: "provisioners/nginx-install.sh"
vagrant reload
vagrant ssh:$ nginx -v
