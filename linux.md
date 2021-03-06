## Linux/Ubuntu useful stuff (tested on Ubuntu Server 18.x)
All the use of `sudo` down here might be making you nervous, but in an ideal Ubuntu setup, you'll make an admin user that isn't root. So this isn't so bad. See this [Digital Ocean guide](https://www.digitalocean.com/community/tutorials/how-to-create-a-sudo-user-on-ubuntu-quickstart) on making a super user when you first light up your Ubuntu instance.

1.    `sudo apt-get upgrade` (gets system updates)
2.    `sudo apt-get dist-upgrade` (upgrades you to a new version of ubuntu)
3.    `sudo apt-get update` (installs system updates)
4.    `sudo apt autoremove` (cleans up all the old update packages)
5.    `sudo apt-get program-name-here` (if the program has a binary build, you get it via this command)
6.    `sudo add-apt-repository ppa:webupd8team/sublime-text-2;` (gets you sublime text but any repo could be put here after the ppa: part)
7.    `sudo apt-get update;` (run update again)
8.    `sudo apt-get install sublime-text` (installs sublime)
9.    `sudo apt-get install xsel` (helps get you pbcopy on ubuntu)
10.    `alias pbcopy='xsel --clipboard --input'` (gets you pbcopy)
11.    `alias pbpaste='xsel --clipboard --output'` (gets you pbpaste)
12.    `sudo whereis your-filename-here` (tells you where a certain file is, but it really doesnt work)
13.    `sudo /usr/share/webmin/changepass.pl /etc/webmin root new-password` (changes your webmin password, which is similar to an act of god)
14.    `sudo a2enmod rewrite` (sets up rewrite_mod for Apache2 - this powers pretty URLs in many CMSs)
15.    `/Applications/VirtualBox.app/Contents/MacOS/VBoxGuestAdditions.iso` (path for virtual box guest additions if you are running an Ubuntu dev machine from OSX)
16.    `CNTL+H in file browser` (shows hidden files in Ubuntu)
17.    `sudo ufw allow 80/tcp` (adds typical port 80 to allowable ports list on ufw, which is ubuntu firewall)
18.    `sudo ufw show added` (shows which ports you have allowed on ufw)
19.    `sudo ufw enable` (enables ufw)
20.    `sudo fallocate -l 4G /swapfile` (creates 4G swapfile)
21.    `sudo chmod 600 /swapfile` (puts proper permissions on the swapfile directory so the world cant see it)
22.    `sudo mkswap /swapfile` (format the folder for swap usage)
23.    `sudo swapon /swapfile` (enable swapfile)
24.    `sudo sh -c 'echo "/swapfile none swap sw 0 0" >> /etc/fstab'` (makes ubuntu server automatically load it's swap file on restart)
25.    `sensors` (gives you readout on CPU core temps)
26.    `lscpu` (details on CPU hardware and frequency utilization)
27.    `sudo hddtemp /dev/sda /dev/sdb /whatever/your/drive/name/is` (gives you temperature info on HDDs)
28.    `lsusb` (tells you which devices are connected to your linux install)
29.    `sudo lshw -short` (gives you read out of all your hardware)

Using Handbrake

1) Find out where you DVD drive is on your server
`sudo lshw -short`

2) Locate the drive for `lshw` command and find the 'device' path, should be something like:
`/dev/cdrom`

3) Manually, make a mount point for the drive on your system (should probably be at root)
`sudo mkdir /mounted/cdrom`

4) Mount drive to mount point
`sudo mount -t auto /dev/cdrom /mounted/cdrom`

5) Install HandBrake repo 
`sudo add-apt-repository ppa:stebbins/handbrake-releases`
`sudo apt-get update`

6) Install HandBrakeCLI
`sudo apt install handbrake-cli`

7) Most DVDs are locked, libdvdcss decodes them
`sudo apt install libdvd-pkg && sudo dpkg-reconfigure libdvd-pkg`

8) Uses HandbrakeCLI to rip movie (-i path/to/mounted/dvd, -o output/destination, -e video-encoding-format, -q quality, -b audio-bit-rate-aac)
`HandBrakeCLI -i /mounted/cdrom/VIDEO_TS -o /media/video/your_movie_here.mp4 -e x264 -q 22 -B 160`
