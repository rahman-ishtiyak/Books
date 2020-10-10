

	============================= Used Frequently =============================

			sudo pacman -Scc
			sudo pacman -Sc
			sudo pacman -Syu
			yaourt -Qdt
			sudo paccache -ruk0
			sudo paccache -rk 1
			paccache -rvk2
			sudo ls /var/cache/pacman/pkg/ | wc -l
			du -sh /var/cache/pacman/pkg/
			sudo paccache -r
			sudo journalctl --vacuum-size=50M
			sudo pacman -Rsn $(pacman -Qdtq)
			
			sudo pacman-mirrors -g
			sudo pacman-mirrors -g && sudo pacman -Syy
			sudo pacman-mirrors --fasttrack 5 && sudo pacman -Syyu
			
        ---------- Install Pamac Package Manager for Aur Support ------------
                        yaourt -S pamac-aur
                        (sudo pacman -S yaourt) -not

			============== Cleaning the cache ============


* Leaves packages in your cache only for those packages which are currently installed on your system. Attention: This eliminates the possibility to Using Downgrade:
			pacman -Sc

* Clean cache completely and remove all packages. Attention: This eliminates the possibility to Using Downgrade:
			pacman -Scc

* A safer way to remove old package cache files is to remove all packages except for the latest three package versions:
			paccache -rvk3

* Get a list of installed packages
			pacman -Q

* List all installed packages from the AUR
			pacman -Qem


		=========== Improve download and database access speed ============

* Ranking mirror list:
			sudo pacman-mirrors --fasttrack 5 && sudo pacman -Syyu

* Optimize the database access speed:
			pacman-optimize && sync

* Commands for syncronising database:
			pacman -Sy

* You can force sync the database using the following command. It means, the database will be synced even if it's up to date. This is useful when you changed something repository related and want to have the changes take effect:
			pacman -Syy


	================= Commands for updating the system =================

* Never use this command as it might result in partial updates:
			pacman -Su

* The recommended way is to syncronize your repo databases first and the update:
			pacman -Syu

* If you have used pacman-mirrors to recreate the mirror list you must download the databases and the update:
			pacman -Syyu


		===================== Installing Packages =============

* Install a package:
			pacman -Syu package_name

* Install packages as a group:
			pacman -Syu gnome
			pacman -Syu kde

* Download a package without installation:
			pacman -Sw package_name
	
	
		==================== Removing Packages =================

* Remove a package:
			pacman -R package_name

* Remove a package with dependencies that are not being used by other packages:
			pacman -Rs package_name

* Remove a package with all dependencies. Attention: The -c flag can remove needed dependencies, too. Only for advanced users.:
			pacman -Rsc package_name

* Remove a package and its configuration files too:
			pacman -Rn package_name

