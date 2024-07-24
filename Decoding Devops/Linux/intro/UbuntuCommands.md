- # Users
	- instead of useradd
		- adduser <user_name>
			- this creates all necessary dirs, groups, etc...
		- ![[Pasted image 20240721195727.png]]
- # visudo
	- export EDITOR=vim 
		- default editor becomes vim (only for current session)
- ## Installing packages
	- wget <binary_file_url>
	- dpkg -i <output_.deb_file> 
	- installed
	- or apt-get <_name_>
- ## Using apt
	- /etc -> configuration files
	- /etc/apt/sources.list -> all installed repositories 
	- apt purge <package_name>:
		- cleanly removes everything from the package such as confg files