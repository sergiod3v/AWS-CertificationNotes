![[Pasted image 20240724112234.png]]
here the nginx app gets the exposed tomcat application and routes it through its proxy so its accssible and more services can be routed to nginx
it uses the hostname configured in /etc/hosts (app 01)

7f7e9a0  default virtualbox poweroff C:/vagrant-vms/ubuntu

b1cfe35  default virtualbox poweroff C:/vagrant-vms/centos

90db2a4  default virtualbox poweroff C:/vagrant-vms/wordpress

72df78a  default virtualbox poweroff C:/vagrant-vms/financeIAC

e4d44ad  default virtualbox poweroff C:/vagrant-vms/wordpressIAC

vagrant destroy 7f7e9a0 
vagrant destroy b1cfe35 
vagrant destroy 90db2a4 
vagrant destroy 72df78a 
vagrant destroy e4d44ad 