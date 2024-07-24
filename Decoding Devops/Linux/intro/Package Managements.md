| **Distribution**                    | **Package Manager**                     | **Package Format**             | **Installation Command**                                         |
| ----------------------------------- | --------------------------------------- | ------------------------------ | ---------------------------------------------------------------- |
| Ubuntu                              | APT (Advanced Package Tool)             | .deb (Debian package)          | `sudo dpkg -i package.deb` and `sudo apt install ./package.deb`  |
| Debian                              | APT (Advanced Package Tool)             | .deb (Debian package)          | `sudo dpkg -i package.deb` and `sudo apt install ./package.deb`  |
| Fedora                              | DNF (Dandified Yum)                     | .rpm (Red Hat Package Manager) | `sudo dnf install package.rpm`                                   |
| CentOS                              | YUM (Yellowdog Updater, Modified) / DNF | .rpm (Red Hat Package Manager) | `sudo yum install package.rpm` or `sudo dnf install package.rpm` |
| Red Hat Enterprise Linux (RHEL)     | YUM / DNF                               | .rpm (Red Hat Package Manager) | `sudo yum install package.rpm` or `sudo dnf install package.rpm` |
| openSUSE                            | Zypper                                  | .rpm (Red Hat Package Manager) | `sudo zypper install package.rpm`                                |
| Arch Linux                          | Pacman                                  | .pkg.tar.zst (Pacman package)  | `sudo pacman -U package.pkg.tar.zst`                             |
| Manjaro                             | Pacman                                  | .pkg.tar.zst (Pacman package)  | `sudo pacman -U package.pkg.tar.zst`                             |
| Gentoo                              | Portage                                 | Source-based (ebuilds)         | `emerge package`                                                 |
| SUSE Linux Enterprise Server (SLES) | Zypper                                  | .rpm (Red Hat Package Manager) | `sudo zypper install package.rpm`                                |

- Installing with RPM packages
	- curl <_.rpm_file_download_url_> -o _**<rpm_output_file_path>**_
	- rpm -ivh _**<rpm_output_file_path>**_
		- -ivh:
			- i: install
			- v: verbose
			- h: human readable
		- install and output readble result
	- ### Solving dependency problem
		- use package manager like yum for centos

# Installation Commands for [Jenkins](https://www.jenkins.io/doc/book/installing/linux/#red-hat-centos)

![[Pasted image 20240721183909.png]]

| **Step**                               | **Command**                                                                  | **Purpose**                                                                                  |
| -------------------------------------- | ---------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| Fetch Jenkins Repository Configuration | `sudo wget -O <desired location for output> <repo location for the package>` | Downloads the Jenkins repository configuration file.                                         |
| Import the GPG Key                     | `sudo rpm --import <public package key>`                                     | Imports the GPG key to verify package integrity and authenticity.                            |
| Upgrade All Installed Packages         | `sudo yum upgrade`                                                           | Updates all existing packages to their latest versions.                                      |
| Install Required Dependencies          | `sudo yum install fontconfig java-17-openjdk`                                | Installs necessary dependencies for Jenkins.                                                 |
| Install Jenkins                        | `sudo yum install jenkins`                                                   | Installs Jenkins, verifying the package with the imported GPG key.                           |
| Reload System Daemon                   | `sudo systemctl daemon-reload`                                               | Reloads the systemd manager configuration to apply changes made by the Jenkins installation. |
