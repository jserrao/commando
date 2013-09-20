// Ubuntu
001.    sudo apt-get upgrade (gets system updates)
001b.	sudo apt-get dist-upgrade (upgrades you to a new version of ubuntu)
002.    sudo apt-get update (installs system updates)
003.    sudo apt-get program-name-here (if the program has a binary build, you get it via this command)
004a.   sudo add-apt-repository ppa:webupd8team/sublime-text-2; (gets you sublime text but any repo could be put here after the ppa: part)
004b.   sudo apt-get update; (run update again)
004c.   sudo apt-get install sublime-text (installs sublime)

// Adds pbcopy to ubuntu
005a.   sudo apt-get install xsel
005b.   alias pbcopy='xsel --clipboard --input' (gets you pbcopy)
005c.   alias pbpaste='xsel --clipboard --output' (gets you pbpaste)

006.    sudo whereis your-filename-here (tells you where a certain file is, but it really doesnt work)
007.    sudo /usr/share/webmin/changepass.pl /etc/webmin root new-password (changes your webmin password, which is similar to an act of god)
008.    sudo a2enmod rewrite (sets up rewrite_mod for Apache2 - this powers pretty URLs in many CMSs)
009.    /Applications/VirtualBox.app/Contents/MacOS/VBoxGuestAdditions.iso (path for virtual box guest additions if you are running an Ubuntu dev machine from OSX)
010.    CNTL+H in file browser (shows hidden files in Ubuntu)