## Basics of the POSIX CLI (command line interface for n00bs)

1.    DONT DO THIS: `rm -rf /` (this means delete everything)
2.    `ssh webadmin@1.2.3.4` (gets you into a server)
3.    `mkdir hello` (make a directory called hello)
4.    `cd hello` (changes your directory to hello, assumes it has been created)
5.    `pwd` (prints path)
6.    `rm your-filename-here` (remove filename (BE CAREFUL!)
7.    `rmdir` - remove directory, if empty
8.    `rm -rf directory/xyz` (removes whole directory with stuff in it)
9.    `rm *.php` (removes all files of that type in one directory)
10.    `man your--program-here` (shows you manual for that part)
11.    `cd ..` (jumps you back a directory)
12.    `cd ../..` (jumps you back two directories)
13.    `cd` (jumps you back to the home directory)
14.    `cd /` (take you to the root directory)
15.    `cd /home/your-username-here` (!where you are!)
16.    `mv /path/goes/here/filename /path/goes/here/your-file-name-2`  (mv moves a file)
17.    `cp /path/goes/here/filename /path/goes/here/your-file-name-2` (copies file in same folder)
18.    `cp -a /path/goes/here/. /path/goes/here/` (copies the contents of an existing folder into a previously defined folder)
19.    try to put a first letter on the line, then use TAB key and it tries to autocomplete - nice!
20.    `find -name hosts` (get)
21.    `sudo` (switch user, do xyz...)
22.    `/etc/hosts` (where the host file lives)
23.    `/etc/init/d` (the folder usually the daemon to start programs live)
24.    `/etc/init.d/sendmail start` (starts mail on server)
25.    `~/` (Shortcut to go home directory of a given user)
26.    `Control + C` (kills the process on the command line)
27.    `Command + K` (OSX clears Bash cache)
28.    `Control + L` (clears the terminal window)
29.    `gzip PATH-HERE` - gzips a file for you, which is what phpmyadmin seems to like
30.    `mysql -uUSERNAME -pPASSWORD DATABASENAME < MYDATABASE.sql` (imports a DB)
31.    `host your-domain-here` (shows you how the DNS resolves)
32.    `shift+control+v` (paste into terminal, OSX)
33.    `chmod +x or chmod 777` (execute permission to make scripts happen)
34.    `cd ~/.ssh` (see if you have ssh keys installed)
35.    `ssh-keygen -t rsa -C "youremail@host.com"` (installs SSH keys - needed for git transactions and other stuff)
36.    `source .your-dot-file-here` (this refreshes the file, makes life great)
37.    `sudo your-samba-passwd-here -a quickstart` (changes samba password, allows websites folder in quickstart to appear in mac os x finder)
38.    `ssh your-user-name-here@your-ip-address-here` (logs you into an SSH session)
39.    `ssh root@192.###.###.###` (gives you shell access to a server, will prompt for shell password)
40.    `hostname` (prints your computer's hostname - Linux)
41.    `exit` (logs you out of an SSH session)
42.    `su - username` (switches user to username)
43.    `clear` (erases output in terminal window)
44.    `sudo smbpasswd -a your-name-here` (changes your samba password for file transfer between OSes, good for virtual machines)
45.    `sudo service smbd restart` (restarts samba)
46.    `rvm --default use 2.0.0` (forces Mac OSX to permanently use a newer version of Ruby)
47.    `rvm --default use rubygems 2.0.03` (forces Mac OSX to permantenly use new rubygems - necessary to run Jekyll/Octopress, probably outdated in 2017 but made sense in 2012)
48.    `sudo reboot` (restarts your machine)
49.    `sudo poweroff` (turns off your machine)
50.    `scutil --get HostName` (prints your computer's hostname - OSX)
51.    `scutil --set HostName your-name-hostname-here` (changes your computer's hostname - OSX)
52.    `df` (gives you a readout of the disk space your system has available)
53.    `pwd | pbcopy` (copies your current path in OSX only)
54.    `xcode-select --install` (installs command line tools for xcode - only necessary on osx 10.8 and down, comes standard on osx 10.9 and up)
55.    `chrome://flags` (IN BROWSER WINDOW, NOT COMMAND LINE - you play with chrome's plumbing, like disabling that stupid notifications center that tacked into OSX)
56.    If you install node.js, put it here: `/usr/local/bin/npm`
57.    `npm install -g yo` (if you have node.js, this installs yeoman, bower and grunt)
58.    `npm install -g generator-webapp` (puts scaffolding in for creating webapps)
59.	   `sudo chown your-user-name-here /usr/local/your/root/path/here` (changes ownership of various files via CLI)
60.    `pbcopy < ~/.ssh/id_rsa.pub` (copies something to your clipboard, so you can paste it like a human being - only in OSX. This example copies your SSH key.)
61.    `cat` - concatenate the key (for example, cat ~/.ssh/id_rsa.pub ), prints my ssh key
62.    `/etc` (is a symlink to /private/etc - Mac OSX sets this up natively)
63.    `/private/etc/apache2/httpd.conf` (where the Mac OSX native apache files live)
64.    `wget -mirror $url` (replicates site in your local folder - whichever folder you run the command from)
65.    `gpasswd -a username-here sudo` (adds a user to sudo group, must be `root`)
66.    `adduser username` (adds user to ubuntu)
67.    `ls -a` (shows all files, including hidden ones)
68.    `curl -I https://your-url-here.whatever` (gives you the HTTP headers for a given request)
69.    `<Return> ~ .` (kills an open ssh session)
70.    `service mysqld start` (starts up the mysql server, assumes mysql is installed on the box)
71.    `ls` (spits out list of directory view)
72.    `scp -r /Users/username-here/desktop/source ssh-username-here@ftp.domain.com:/home/user/public_html/dir/destination` (scp securely copies a directory from one place to another - the directory on the left is the SOURCE, the right is the DESTINATION)
73.    `pwd | tr -d '\n' | pbcopy` (copies command line path in OSX - h/t: bradlanders.com) - make an alias of this so its less crazy next time: alias cpwd="pwd | tr -d '\n' | pbcopy"
74.    `cpwd` (will copy a path to your clipboard, after you make the alias in the above step - aliases will only work locally - YOUVE BEEN WARNED!)
75.    `service httpd start` (starts your apache server, assumes apache is installed on the box)
76.    `ssh -p #### username-here@server-name-here` (connect to a specific port (non-22) on a ssh server)
77.    `htpasswd -c /user/your-name-here/domain.com/.htpasswd admin` (sets up the encrypted .htpasswd file youll need to password protect your apache-based server - will prompt for password, assumes you have apache 2.x installed on your server)
78.    `tar -cvzf youfilename-here-dump.tar.gz /home/your/path/here` (tars up a directory for you)  
79.    `ln -s /path/to/file /path/to/symlink` (links file to a path with symlink)
80.    `/System/Library/PrivateFrameworks/Apple80211.framework/Versions/Current/Resources/airport -I | awk '/ SSID/ {print substr($0, index($0, $2))}'` (OSX ONLY! - gets you the SSID of the wireless network you are on)
81.    `/var/www/html or /usr/local/apache/htdocs` (This is where your website should/could live on a linux server. Paths are from the root)
82.    `cd "Foldername with a Space"` (must use quotes to espace space characters on the command line)
83.    `cd volumes` (access remote drives - if already mounted, they will be at volumes/drive-name-nere)
84.    `ls -a` (shows list of files in your directory, including hidden dot files)
85.    `openssl req -new -newkey rsa:2048 -nodes -out star_example_com.csr -keyout star_example_com.pem -subj "/C=country-code-here/ST=state-code-here/L=city-here/O=organization-here/OU=organization-dept-here/CN=*.example.com/emailAddress=team@example.com"` (openssl command to generate a self-signed certificate and private key, note the CN part of command must match the type of SSL cert you need, single or multi-domain)
86.    `sudo easy_install pip` (installs pip, package manager for python)
87.    `alias custom-name-here="cd /Users/you/some/path/here"` (structure for making an aliased path, must be saved into OSX user's .profile file or it will not persist beyond current session)
88.    `sudo apt-get update` (does simple updates, ubuntu)
89.    `sudo apt-get dist-upgrade` (does all the updates, ubuntu)
90.    `sudo apt autoremove` (cleans up all the old update packages)

## Linux/Ubuntu useful stuff (tested on Ubuntu Server 18.x)
All the use of `sudo` down here might be making you nervous, but in an ideal Ubuntu setup, you'll make an admin user that isn't root. So this isn't so bad. See this [Digital Ocean guide](https://www.digitalocean.com/community/tutorials/how-to-create-a-sudo-user-on-ubuntu-quickstart) on making a super user when you first light up your Ubuntu instance.

01.    `sudo apt-get upgrade` (gets system updates)
02.	   `sudo apt-get dist-upgrade` (upgrades you to a new version of ubuntu)
03.    `sudo apt-get update` (installs system updates)
04.    `sudo apt-get program-name-here` (if the program has a binary build, you get it via this command)
05.    `sudo add-apt-repository ppa:webupd8team/sublime-text-2;` (gets you sublime text but any repo could be put here after the ppa: part)
06.    `sudo apt-get update;` (run update again)
07.    `sudo apt-get install sublime-text` (installs sublime)
08.    `sudo apt-get install xsel` (helps get you pbcopy on ubuntu)
09.    `alias pbcopy='xsel --clipboard --input'` (gets you pbcopy)
10.    `alias pbpaste='xsel --clipboard --output'` (gets you pbpaste)
11.    `sudo whereis your-filename-here` (tells you where a certain file is, but it really doesnt work)
12.    `sudo /usr/share/webmin/changepass.pl /etc/webmin root new-password` (changes your webmin password, which is similar to an act of god)
13.    `sudo a2enmod rewrite` (sets up rewrite_mod for Apache2 - this powers pretty URLs in many CMSs)
14.    `/Applications/VirtualBox.app/Contents/MacOS/VBoxGuestAdditions.iso` (path for virtual box guest additions if you are running an Ubuntu dev machine from OSX)
15.    `CNTL+H in file browser` (shows hidden files in Ubuntu)
16.    `sudo ufw allow 80/tcp` (adds typical port 80 to allowable ports list on ufw, which is ubuntu firewall)
17.    `sudo ufw show added` (shows which ports you have allowed on ufw)
18.    `sudo ufw enable` (enables ufw)
19.    `sudo fallocate -l 4G /swapfile` (creates 4G swapfile)
20.    `sudo chmod 600 /swapfile` (puts proper permissions on the swapfile directory so the world cant see it)
21.    `sudo mkswap /swapfile` (format the folder for swap usage)
22.    `sudo swapon /swapfile` (enable swapfile)
23.    `sudo sh -c 'echo "/swapfile none swap sw 0 0" >> /etc/fstab'` (makes ubuntu server automatically load it's swap file on restart)
24.    `sensors` (gives you readout on CPU core temps)
25.    `lscpu` (details on CPU hardware and frequency utilization)
26.    `sudo hddtemp /dev/sda /dev/sdb /whatever/your/drive/name/is` (gives you temperature info on HDDs)

## Linux/Ubuntu - Commands for making a RAID array

Digital Ocean has a [fantastic guide](https://www.digitalocean.com/community/tutorials/how-to-create-raid-arrays-with-mdadm-on-ubuntu-16-04) for doing this with `mdadm`, the Linux RAID utility. Read it.

01. `lsblk -o NAME,SIZE,FSTYPE,TYPE,MOUNTPOINT` (shows you what's going on with your computer's hard drives). Output will look something like this - this shows three drives. `sda` and `sdb` are identical unformatted 4TB HDs while `sdc` is a 128GB SSD with an Ubuntu bootable partition and a swap space setup for when memory runs low):

```
NAME     SIZE FSTYPE TYPE MOUNTPOINT
sda      3.7T        disk
sdb      3.7T        disk
sdc    119.2G        disk
├─sdc1   512M vfat   part /boot/efi
├─sdc2 102.9G ext4   part /
└─sdc3  15.9G swap   part [SWAP]
```

02. `sudo mdadm --create --verbose /dev/md0 --level=1 --raid-devices=2 /dev/sda /dev/sdb` (Assuming the above drive setup, this command uses Linux's mdadm RAID creation utility to create an array. Here we are creating a RAID1 array with the `--create` flag, which means each byte saved to the array gets saved to each disk which creates a backup. You set the type of RAID array you want with the `--level=1` flag, which indicates a RAID1 array. We're striping two drives, so `--raid-devices=2` flag is set to 2. `/dev/sda /dev/sdb` describes the locations of the two drives we determined with the `lsblk` command.

03. `cat /proc/mdstat` (this command shows you where your striping process is at - this can take hours depending on the size of your drives. With 4TB 5400RPM SATA3 drives, this took about 8 hours for me). 

04. `sudo mdadm --detail --scan` (shows you what's going on with your RAID array). Output looks like this: 

```
ARRAY /dev/md/array-name metadata=1.2 name=server-name:array-name UUID=big:alphanumberic:string:here
```

## Ansible / Vagrant
01.    `sudo pip install ansible` (uses pip to install ansible)
02.    `sudo pip install ansible --upgrade` (pip to update ansible)
03.    `vagrant up (turns on your vagrant instance` - must be in directory with vagrantfile)
04.    `vagrant down (turns off your vagrant instance` - must be in a directory with vagrant file)
05.    `vagrant ssh` (ssh's you into your vagrant instance)
06.    `ansible-vault encrypt .your-file-here` (uses ansible-vault to encrypt a file with passwords)
07.    `ansible-vault view .your-file-here` (uses ansible-vault to view an encrypted pw file)
08.    `ansible-vault edit .your-file-here` (allows you to edit a vault pw file)

## AWS CLI
01.    `curl "https://s3.amazonaws.com/aws-cli/awscli-bundle.zip" -o "awscli-bundle.zip"` (downloads AWS bundle, requires python and pip)
02.    `unzip awscli-bundle.zip` (unzips AWS)
03.    `sudo ./awscli-bundle/install -i /usr/local/aws -b /usr/local/bin/aws` (installs bundle)
04.    `aws configure --profile user` (sets up access key ID, secret access key, aws region and output format defaults for using AWS CLI)
05.    `aws ec2 describe-instances --profile user-name` (shows you config profile for a given user on a given AWS service, ec2 in this example)
06.    `aws iam upload-server-certificate --server-certificate-name STAR_example_com --certificate-body file://STAR_example_com.crt --private-key file://star_example_com.pem --certificate-chain file://ca-chain-amazon.crt --path /cloudfront/*/` (uploads an SSL certificate to AWS IAM service)
07.    `aws iam update-server-certificate` (updates AWS IAM SSL certificates)
08.    `aws iam get-server-certificate --server-certificate-name STAR_example_com` (gets you the details of a current SSL certificate)

## Front-end Tooling

01.    `sudo gem install sass` (installs the CSS preprocessor SASS - you need to have Ruby + RVM installed first)
02.    `sass -v` (calls up the sass version)
03.    `grunt test` (preps your app for deployment)
04.    `grunt server` (gets your localhost going)
05.    `grunt whatever-command-you-want-here --force` (flag will override verbose testing periods)
06.    `bower search` (shows entire bower JS library)
07.    `bower search your-JS-package-here` (searches the directory)
08.    `bower install your-JS-package-here` (adds a JS dependency to the project in your folder, works in conjunction with Yeoman)
09.    `bower install your-js-package-here --save` (adds your package into bower.json dependency list)    	
10.    `npm install -g yo generator-wordpress` (installs the community's favorite wordpress yeoman generator - assumes you have yeoman and npm installed)
11.    `npm install -g http-server` (adds a local server you can just spin up)
12.    `http-server /your/path/here` (starts up at localhost:8080 that points at whatever path you tell it, simple server)
13.    `http-server /your/path/here -p 5000` (starts up at localhost:5000, different path declaration)
14.    `apachectl start` (starts http server at http://localhost)
15.    `apachectl stop` (stops http server at http://localhost)
16.    `apachectl restart` (restarts your server)


## GIT! (super useful to do this on the command line versus GUI)

00.	  `brew install git` (installs git, assumes you have homebrew)
01.   `git config --global user.name "Your Name"` (tells Git what your name is)
02.   `git config --global user.email "your_email@whatever.com"` (tells Git what your email is)
03.   `git init` (creates a repository of the current directory)
04.   `git add your-filename-here` (adds a new file)
05.   `git commit -m "First Commit"` (Commits file with a message in quotes)
06.   `git status` (tells you all about the git repositories' files).   git diff head (shows me whats different between whats getting committed and whats in there now)
07.   `git add` (stages changes to your repository BUT does not officially add them yet)
08.   `git add --all` (stages ALL changes to your repository, new in Git 2.0)
09.   `git reset HEAD filename-here` (undoes / unstages changes before they are committed). If you dont specify a comment, the system will drop you into Vim (text editor).  Hit ESCAPE key to change modes after inserting text...
10.   `git remote add local-repo-name-here git@github.com:your-name-here/repo-name-here.git` (basically this means you're connecting git to a remote git repository)
11.   `git remote add --mirror=push repo-name-here git@your.server.here:/your-repo-here.git` (establishes that your local is going to push to the remote)
12.   `git push local-repo-name-here master` (pushes my local up to github, 'local-repo-name-here MUST be the name of your repo')
13.   `git stash save` (will save changes that are not committed yet, like a faux branch)
14.   `git remote -v` (tells you what remote repos are connected to your local repo)
15.   `git config --global color.ui true` (sets up the cool command line color coding)
16.   `/home/your-name-here/.ssh/id_rsa.pub` (this is where you SSH keys live, youll have to hand the public side of your key to github)
17.   `git clone git://repo-url-goes-here.git destination-folder-here` (just put a space after the standard clone command to get a nice destination folder)
18.   `git clone -b branch-here remote-repo-here` (clone a remote branch)
19.   `git submodule add https://github.com/user-name-here/repo-name-here /destination/directory/here` (puts a git submodule into your current repo)
20.   `(FORCE FLAG example) git submodule add -f repo-here directory-here` (-f forces something to be added, even over the .gitignore file)
21.   `git status -s` (does a shorter version of the status thing)
22.   `git remote add origin https://github.com/user-name-here/repo-name-here`
23.   `git remote set-url -add origin https://github.com/user-name-here/repo-name-here` (specifically set's the URL for a remote repo, 'origin' in this case)
24.   `git push origin master` (pushes your code up to a remote, 'origin' is remote, 'master' is your local branch - must setup a remote beforehand)
25.   `git add -u` (adds deleted files into the commit)
26.   `git config core.autocrlf false` (fixes line ending errors)
27.   `git config core.safecrlf warn` (allows git to actually convery CRLF (win) to LF (linux/osx) line endings)
28.   `git config --global --add color.ui true` (turns git's coloring on)
29.   `git rm file-name-here.txt` (removes file | directory from the repo)
30.   `git ls-tree --full-tree -r HEAD` (list of all files in your repo)
31.   `git branch` (shows you a list of all branches; the one with a '*' is your current branch)
32.   `git tag -a v1.4 -m 'my version 1.4'` (tags your branch with a version)
33.   `git show v0.1` (git will show whats going on with a given tag)
34.   `git rm -r -f .sass-cache/` (recursively removes a whole bunch of junk from your repo)
35.   `git branch your-branch-here` (makes a new branch)
36.   `git checkout your-branch-here` (switches to doing commits against that branch)
37.   `git checkout -b your-name-here/your-topic-here` (establishes a new branch and switches to it so that future commits will be made against it)
38.   `git remote -v` (shows you all of your remotes)
39.   `git stash clear` (deletes everything off of stash)
40.   `git merge branch-name-here` (will merge branch-name-here with whatever branch you are on, do 'git pull' on your branch and make sure it's up to date with origin before merging!)
41.   `git reset --hard \[hash\]` (resets git to a given commit in the past on your branch)
42.   `git branch -v` (shows all branches, active one has '*' next to its name)
43.   `git log -n 5 --author=your-name-here` (shows the last 5 commits from a given author)
44.   `git reset` (undoes whatever you staged, all of it)
45.   `git push origin --delete your-branch-here` (deletes remote branches)
46.   `git branch -D your-branch-here` (deletes local branches, overrides conflicts)
47.   `git branch -d your-branch-here` (deleter local branches, will stop if uncommited changes are on branch)
48.   `echo .DS_Store > ~/.gitignore_global` (creates a global .gitignore_global file to store files you never want in your repo)
49.   `git config --global core.excludesfile ~/.gitignore_global` (will permanently ignore .DS_Store files in OSX)
50.   `git checkout --track origin/your-branch-here` (pulls in new remote branch to your local repo)
51.   `git remote rename old-repo-here new-repo-here` (renames your remote repo)
52.   `git stash apply` (puts uncommitted changes back onto current branch from stash)
53.   `git fetch` (pull all code off remote and puts it into a local cache, updates synced local branches)
54.   `git branch --track branch-name origin/branch-name` (if you don't have local branches synced with remotes, you can now sync them with this baby)
55.   `git submodule update --remote` (supposedly updates all submodules from .gitmodules, I have my doubts)
56.   `git add .`
57.   `git commit -m "Updated submodule"`
58.   `git push --follow-tags` (how to push tags to remote - they don't go with your code)
59.   `git fetch origin` (grabs all the stuff on your remote that isn't in your repo, puts it into a cache of sorts)
60.   `git checkout xyz` (creates tracking branch for whatever you fetched)
61.   `git branch --unset-upstream` (remove tracking branch's link to remote branch)
62.   `git rm --cached myfile.log` (removes file from repo cache, which is usually why you see .gitignore failures)
63.   `git rev-list --count branch-name-here` (shows you how many commits are in a given branch)
64.   `git push -f <remote> <branch>` (forces an overrite of remote with your branch, BE CAREFUL)
65.   `git rm -r --cached myFolder` (removes files from git repo but not filesystem - so they are there just not tracked. To me this implies that you should also be added whatever folder removed with this method into your .gitignore file).
66.   `git remote rename your-old-name-here your-new-name-here (rename remote)
67.   `curl -u 'USER' https://api.github.com/user/repos -d '{"name":"REPO"}'` (Using GitHub API v3 to create a repo from terminal without using web interface. Then 'git remote add')
68.   `git fetch <remote> <remote-branch>:<local-branch>` (creates a real local branch of a remote repo, not tracking branch)


## Heroku (Salesforce app cloud)
00.    `wget -qO- https://toolbelt.heroku.com/install-ubuntu.sh | sh` (installs heroku toolbelt, assumes you have wget which you can install via homebrew if needed)
01.    `heroku login` (will log you into your apps, prompts heroku info)
02.    `git push heroku-test next-release:master` (this will deploy from branch next-release to branch master, where heroku-test is your server for deployment)
03.    `heroku certs:update --app app-name STAR_example_com.crt private.pem` (updates Heroku SSL certificate for a given environment, after --app flag, app-name, cert-file, key-file in that order)
04.    `heroku git:remote -a your-environment-name-here -r custom-environment-name-here` (adds a heroku remote to your repo, -a flag is server name, -r is custom name for the server)
05.    `heroku restart -a app_name` (restarts your app dyno, very quickly)

## Homebrew (package manager for Mac)
00.	   `ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"` (installs homebrew)
01.	   `brew doctor` (tells you whats wrong with homebrew's formulas, whats going in the 'cellar')
02.    `brew update` (updates homebrew)
03.    `brew upgrade your-package-here` (updates a given brew, like node, npm, yeoman, etc)
04.    `brew link --overwrite your-package-here` (forces symlink creation)
05.    `brew prune` (removes dead symlinks)
06.    `brew [whatever] --dry-run` (tells you whats going to happen before you do it)
07.    `brew install your-package-here` (installs whatever you want via homebrew, be careful when you install node via homebrew - leave npm out of the install and [follow these instructions] (https://gist.github.com/DanHerbert/9520689))
08.    `/usr/local/Cellar` (where Homebrew installs stuff)
09.    `/usr/local/var/your-program-here` (another place Homebrew apparently installs stuff)
09.    `users/your-macosxname-here/.node` (where Homebrew puts node's stuff, if you install via homebrew - you shouldnt do this! Use the node OSX installer instead)
10.    `users/your-macosxname-here/.node/lib/node_modules` (where npm installs stuff if you use Homebrew)

## Lando, replacement for Kalabox - local dev with Docker containers, very slick
01.   `lando` (hello world more or less)
02.   `lando config` (shows you version of kalabox)
03.   `lando status` (tells you if the docker engine is up/down)
05.   `lando start` (takes docker engine online)
06.   `lando stop` (takes docker engine offline, good for resets)
07.   `lando push` (moves local code to pantheon, slick - it will ask via prompts)
08.   `lando pull` (take code from dev it will also ask via prompts)
09.   `lando pull --database=dev --files=dev` (pulls code, DB and files from Pantheon to your local)
10.   `lando switch your-multidev-branch` (switches code and DB over to pantheon multidev branch)
11.   `lando wp cache flush` (empties wp cache, good if you're using redis plugin for Pantheon)

## Lando - steps to creating a local Pantheon instance
01.   `git clone ssh://codeserver.dev.uniqueID@codeserver.dev.uniqueID.drush.in:2222/~/repository.git` (clone your git repo from Pantheon into `sites/your-site-here`)
02.   `lando init` (run this command in `sites/your-site-here` and lando will put together a `.lando.yml` when you select 'Pantheon' from its list of valid recipes. You may have to setup a machine token through Pantheon if you haven't connected Pantheon and Lando together before)
03.   `git add . && git commit -m 'My lando setup'` (put the lando setting into your repo, commit)
04.   `lando pull` (this will walk you through pulling your files and DB from Pantheon. If this app is in production, pull the prod DB and prod files)
05.   `lando start` (you'll kick start the Docker server and it will set itself up, you should be good now)

## Lando - steps to creating a local WordPress instance, big difference is DB setup
01.   `git clone git@github.com:username/reponame.git` (clone your git repo from Github into `sites/your-site-here`)
02.   `lando init` (run this command in `sites/your-site-here` and lando will put together a `.lando.yml` when you select 'WordPress' from its list of valid recipes.)
03.   Customize your `.lando.yml` to match your production environment as best you can. If you aren't using a container-based host like Pantheon, you won't get 1:1 parity. For WP-Engine, I used these settings:

```
# Site name
name: your-site-name-here

# Start with the default WordPress recipe
recipe: wordpress

# Configure the WordPress recipe
# See: https://wordpress.org/about/requirements/
# I'm trying to match up with wpengine settings as best I can
config:

  # Optionally specify the php version to use.
  #
  # If ommitted this will default to the latest php version supported by WordPress.
  # Consult the `php` service to see what versions are available. Note that all
  # such versions may not be supported in WordPress so YMMV.
  #
  # See: https://wordpress.org/about/requirements/
  #
  # NOTE: that this needs to be wrapped in quotes so that it is a string
  php: '7.0'

  # Optionally specify whether you want to serve drupal via nginx or apache
  # If ommitted this will default to the latest apache
  # See: https://wordpress.org/about/requirements/
  via: nginx

  # Optionally activate xdebug
  #
  # If you are having trouble getting xdebug to work please see:
  # https://docs.devwithlando.io/services/php.html#using-xdebug
  xdebug: true
```

04.   `git add . && git commit -m 'My lando setup'` (put the lando setting into your repo, commit)
05.   `lando start` (you'll kick start the Docker server and it will set itself up, but you have no DB or files right now)
06.   Go into your prod server, get your `wp-content/uploads` directory and manually put it into your new Lando install
07.   Do the same thing for your database. You can use CLI mysql of phpMyAdmin, doesn't matter. But put the DB into the root of your project (don't commit it, you'll delete it later - don't freak).
08.   Run `lando info` and note the 'internal connection' settings of the 'database'. Go put that info into your `wp-config.php` - which will look something like this for Lando/WP-Engine environment. Your DB port might be different though:

```
/** The name of the database for WordPress */
define('DB_NAME', 'wordpress');

/** MySQL database username */
define('DB_USER', 'wordpress');

/** MySQL database password */
define('DB_PASSWORD', 'wordpress');

/** MySQL hostname */
define('DB_HOST', 'database:3306');

/** Database Charset to use in creating database tables. */
define('DB_CHARSET', 'utf8');

/** The Database Collate type. Don't change this if in doubt. */
define('DB_COLLATE', '');
```

09.   `lando db-import 2018-02-14-1300-your-database-prod.sql` (This should import your DB and give you an `Import Complete` CLI feedback if you did this right.)
10.   `lando wp search-replace 'your.productiondomain.com' 'your-site-name.lndo.site:444'` (This is a search - replace on the DB, note using the `lando` command first. This fixes the DB in the docker container, which is what you want to do. Where did I get that crazy URL `*.lndo.site:444`? I got it from `lando info` and taking the SSL varient.)
11.   Now if you use a theme with front-end tooling (build tools, Sass, Bower, etc), go into the theme and run the setups. `npm install`, `bower install`, `composer install`, etc. Commit the `*-lock.json` files you get.
12.   Run a `lando rebuild` when you've done all of this. It will reset the DB and all the Docker containers, which I feel like is a good idea after all this crazy shit. Go to `your-site-name.lndo.site:444`, ok the security crap and you should be good to go now. How about that?


## MySQL Server (assumes use of homebrew)
01.   `brew install mysql` (starts mysql package installation via homebrew)
02.   `unset TMPDIR` (run this command immediately after installation)
03.   `mysql_install_db --verbose --user=/`whoami/` --basedir="$(brew --prefix mysql)" --datadir=/usr/local/var/mysql --tmpdir=/tmp` (allows you to actually use mysql with your user account)
04.   `/usr/local/opt/mysql/bin/mysqladmin -u root password 'your-new-password-here'` (sets new root password for mysql on your system)
05.   `/usr/local/opt/mysql/bin/mysqladmin -u root -h MacBook-Pro.local password 'new-password'` (finishes setting up mysql new root password)
06.   `/usr/local/opt/mysql/bin/mysql_secure_installation` (allows for production server-level installation)
07.   `mysqladmin` (command to do just about everything with mysql)
08.   `mysqld` (starts mysql server, but not really a lot of times)
09.   `mysqladmin create your-db-here --port=port-number-here --user=user-name-here --password[=your-password-here] --host=your-hostname-here` (initializes new database, note randomly unique syntax for password - but of course some random shit like this shows up on a CLI command, amiright?)
10.   `mysql -u root -p` (opens up a new kind of terminal command prompt, specific to mysql - will prompt for password (another layer of hell for you to wander through)
11.   `mysql> CREATE DATABASE your-database-name-here;` (at the mysql prompt, this will create your database AFTER you have connected in the step above, don't forget the semicolon)
12.   `mysql> CREATE USER 'new-user-here'@'localhost' IDENTIFIED BY 'your-password-here';` (establishes new user in the DB)
13.   `mysql> GRANT ALL PRIVILEGES ON * . * TO 'new-user-here'@'localhost';` (gives all sql privledges to your new user)
14.   `mysql> FLUSH PRIVILEGES;` (resets db to accept new user)
15.   `mysql> quit;` (lets you leave the mysql specific prompt)
16.   `mysql> USE database-name-here;` (chooses a database to manipulate)
17.   `mysql> mysql -u root -p database-name < database-to-be-imported.sql;` (imports existing mysql DB into mysql itself - note that you must run this command from the folder you are in or change the last part of the command into an actual path)
18.   `mysql> CREATE USER 'username'@'localhost' IDENTIFIED BY 'password-here';` (creates a user with pw on localhost)
19.   `mysql> GRANT ALL PRIVILEGES ON *.* TO 'user'@'localhost' WITH GRANT OPTION;` (gives new user sudo powers)
20.   `mysql> SHOW GRANTS FOR 'user'@'localhost';` (shows you what your new user can do)

## Mongo
01.    `ln -sfv /usr/local/opt/mongodb/*.plist ~/Library/LaunchAgents` (starts Mongo when your computer turns on)
02.    `launchctl load ~/Library/LaunchAgents/homebrew.mxcl.mongodb.plist` (starts Mongo for first time, assumes you installed via Homebrew and uses [OSX CLI tools launchctl launchd] (http://ss64.com/osx/launchctl.html))
03.    `mongod` (starts the mongo server from CLI)
04.    `mongorestore -h dbserver.example.com:port -d db-name-here -u user-here -p password-here local-db-folder-path` (restores DB backup to a mongo server - assumes mongo is installed on destination server)
05.    `mongorestore -h dbserver.example.com:port -d db-name-here -u user-here -p password-here --drop local-db-folder-path` (Before restoring the collections from the dumped backup, drops the collections from the target database. --drop does not drop collections that are not in the backup.When the restore includes the admin database, mongorestore with --drop removes all user credentials and replaces them with the users defined in the dump file)
06.    `mongodump -h example.dbserver.here:port -d db-name -u dbuser-here -p password-here -o output-folder-here` (exports DB to a destination folder - note that mongo does not output a single SQL-like file but a folder of .json and .bson files)
07.    `mongodb://db-user-here:db-password-here@example.db.server.com:port,example2.db.server.com:port/dbname-here` (mongo URI to connect cloud instances - like mongolab > heroku)
08.    `mongo --eval` (gives you ability to insert any mongo query but you dont always need it)
09.    `mongo asdf######.mongolab.com:#####/dbname -u dbuser -p dbpassword` (connect to remote mongo instance on mongolab)
10.    `/usr/local/cellar/mongodb/3.0.3/bin` (where you'll find the core mongo files if you install mongodb via homebrew on OSX - also remember this is where you have to run mongolab connection requests from for whatever reason)
11.    `mongodb://user-name:password@ds123456-a.mongolab.com:27799/db_name_here` (URI string for a mongoDB)


## Mongo Commands
#### very useful (https://docs.mongodb.org/manual/tutorial/write-scripts-for-the-mongo-shell/)
01.    `> db.getUsers()` (tells you who is in the DB)
02.    `> db.createUser({user: "admin", pwd: "password", roles: [ { role: "readWrite", db: "db-name-here" }]})` (assigns user with read/write privledges to db)
03.    `> db.getUser("admin")` (send string of whomever you want to find, tells you about them)
04.    `> db.getCollectionNames()` (gives you a list of all the collections (aka tables) in your DB)
05.    `> db.getUsers()` (gives you a list of all the users)
06.    `> db.collection.update({ "key" : "old-value" },{ $set: { "key" : "new-value" }},{ multi : true })` (sets a new value for all records that match key/old-value pair


## PIP (Python install tool)
01.    `sudo easy_install pip` (this should work on OSX, I needed sudo but maybe you don't? - you could also use homebrew)
02.    `sudo pip install --upgrade pip` (upgrades pip)
03.    `sudo pip list` (shows the packages you have installed)
04.    `sudo pip show ansible` (shows current status on a given package, 'ansible' in this case)

## Terminus (Pantheon CLI)
01.   `terminus auth login your@email.com` (authorizes your machine into pantheon - you need to create a machine token on pantheon.io before this will work)
2.    `terminus sites create --upsteam=#### --site=site-name --label="Something good" --org=your-org-id` (will give you a CLI walkthrough to install an instance on pantheon infrastruture)
3.    `terminus site dashboard --site=yoursitename` (automatically bounces you out to the pantheon dashboard GUI)
4.    `terminus site connection-info --site=yoursitehere --env=dev --field=git_command\` (makes local git repo, NOTE backticks to get this to work)
5.    `terminus wp 'core install --url --url=http://dev-example.pantheonsite.io --title="Name of site" --admin_user=admin --admin_password=somethinggood --admin_email="your@email.com"'` (sets up a wordpress site - not really sure why you wouldnt just use their one button installer but hey, there is a command if you want to make your life harder)
6.    `terminus wp 'plugin install plugin-slug-from-wordpress.com --activate'` (installs plugin but will ask you for Pantheon admin pw for the site)
7.    `terminus build:project:create github-repo-owner/github-repo-name YOUR-SITE-HERE` (builds a Wordpress / Drupal based site on Pantheon)


## Transferring things (SFTP, SCP, rsync)

### SCP
[Everything SCP - go here](http://kb.iu.edu/data/agye.html)
01.    `scp -r local-path-goes-here remote-user@remote-hostname:your-remote-path-goes-here` (EXAMPLE: `scp -r /users/your-name/documents/mapbox/export/tile-set.mbtiles user@61.56.90.123:/home/user/mapbox-tiles/tile-set.mbtiles`, the `-r` makes it recurse through the entire folder)

### SFTP
01.    `sftp your-host-here` (gets you in, will put you at prompt likely need a password or have SSH key in place)
02.    `*ix commands - ls, pwd, cd` (navigate REMOTE folders)
03.    `lls, lpwd, lcd` (anything with `l` in front navigation LOCAL folders)
04.    `put /your/path/here/filename.txt` (puts LOCAL file on the REMOTE server, navigate to where you want the file first!)
05.    `put -r /your/folder/here` (puts LOCAL folder onto the REMOTE server)
06.    `get /your/path/here/filename.txt` (gets REMOTE file and puts it on LOCAL machine)
07.    `get -r /your/folder/here` (gets REMOTE folder and puts it on LOCAL machine)

### rsync (the only way to fly)
01.    `rsync -rv --exclude='.git' /Users/your-name-here/sites/personal/example.com username-here@you-site.com:/home/user/public_html/site-folder` (move a file up to a server via SSH while excluding .git | -r = recursive, -v = verbose output)
03.    `rsync -rv /Users/your-name-here/sites/personal.com/ username-here@you-site.com:/home/user/public_html/site-folder` (NOTE - trailing slash on first path! this moves the contents of the folder, not the folder itself)

## Vim (an annoying text editor)

01.    vim your-filename-here (vim will open OR create file)
02.    DD (delete's the current line)
03.    :w (write file)
04.    :q (quit Vim)
05.    :wq (write/quit Vim)
06.    o (lets you insert text on a new line)
07.    i (lets you insert text on same line)
08.    x (deletes a character)
09.    A (moves you to the end of content)
10.    G (end of line, go into insert mode)
11.    escape (exits you from editing content mode)
12.    :e (new file)
13.    shift + v (selects text - you cant do this while in INSERT mode)
14.    d (cut highlighted text)
15.    P (paste before cursor)
16.    p (paste after cursor)
17.    /your-string (allows you to search for a string)
18.    CTRL + f (page down)
19.    CTRL + b (page up)
