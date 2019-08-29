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