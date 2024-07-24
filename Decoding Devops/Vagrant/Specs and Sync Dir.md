
- # Setting RAM: 
	- ![[Pasted image 20240722091951.png]]
		- ![[Pasted image 20240722093039.png]]
		- ~1.5GB RAM 
		- ![[Pasted image 20240722093148.png]]
		- 2 cores given
	- vb (virtualbox) has attributes
		- memory : RAM
		- cpus: no of cpus
- # Network
	- ![[Pasted image 20240722091835.png]]
	- vm.network "private_network" refers to static private ip the vm will have
	- ![[Pasted image 20240722092756.png]]
		- Adapter 1: NAT, only used by vagrant
		- Adapter 2: private static IP, just specified ("private network")
		- Adapter 3: Bridge, (public ip given by physical router)
- # Sync Dir
	- Vagrant syncs 2 folders, one inside the vm and the other inside the host machine
		- /vagrant/ -> root folder in the vm
	- Set our own synced folder
		- config.vm.synced_folder