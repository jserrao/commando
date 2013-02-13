// SCP
001.    [Everything SCP - go here](http://kb.iu.edu/data/agye.html)
002.    scp -r local-path-goes-here remote-user@remote-hostname:your-remote-path-goes-here (EXAMPLE: scp -r /users/your-name/documents/mapbox/export/tile-set.mbtiles user@61.56.90.123:/home/user/mapbox-tiles/tile-set.mbtiles, the -r makes it recurse through the entire folder)

// SFTP
001.    sftp your-host-here (gets you into)
002.    mput /your/path/here/filename.txt (puts your file on the server, navigate to where you want the file first!)