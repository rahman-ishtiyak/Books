======== Manjaro 10 Things ==========

1. Update Manjaro -
		$ sudo pacman -Syu
		$ sudo pacman -Syyu

	# Install Package Manjaro:
		$ sudo pacman -S <pckage-name>
	# Remove Package Manjaro:
		$ sudo pacman -Rs <package name>
	# Remove Unrequired packages:
		$ sudo pacman -Qdtq
	$ Display package information:
		$ sudo pacman -Si <package name>

2. Configure package manager to add yaourt |

3. Install/Active Firewall - 
	sudo pacman -S gufw

4. Rank Mirrors -
	sudo pacman-mirrors -g

5. Active Infinality fonts -
	sudo leafpad /etc/profile.d/freetype2.sh

6. Gaming setup -
	Install graphics driver, PDL/POL, wine, winetricks, 32bit libs, lib32-libldap

7. Install and configure clamtk

8. Install utilities -
	htop, screenfetch, hardinfo, cherrytree, etcher, wmail

9. Set mirrors to fastest 5
	$ sudo pacman-mirrors --fasttrack 5
	$ sudo pacman -Syyu

10. Switch to testing branch
	$ sudo pacman-mirrors -aB testing
	$ sudo pacman -Syyu

11. Switch to stable branch
	$ sudo pacman-mirrors -c all -aB stable
	$ sudo pacman -Syyu

12. Set Fastest Mirror
	$ sudo pacman-mirrors -f && sudo pacman -Syyu

	$ sudo pacman-mirrors -f0 && sudo pacman -Syyu (*** WORKING ***)