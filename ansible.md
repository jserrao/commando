## Ansible w/ Vagrant
01.    `sudo pip install ansible` (uses pip to install ansible)
02.    `sudo pip install ansible --upgrade` (pip to update ansible)
03.    `vagrant up (turns on your vagrant instance` - must be in directory with vagrantfile)
04.    `vagrant down (turns off your vagrant instance` - must be in a directory with vagrant file)
05.    `vagrant ssh` (ssh's you into your vagrant instance)
06.    `ansible-vault encrypt .your-file-here` (uses ansible-vault to encrypt a file with passwords)
07.    `ansible-vault view .your-file-here` (uses ansible-vault to view an encrypted pw file)
08.    `ansible-vault edit .your-file-here` (allows you to edit a vault pw file)