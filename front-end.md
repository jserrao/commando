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
17.    `nvm ls` (if you installed node vs nvm - and you should - this will show you what versions you have)
18.    `nvm use VERSION` (where `VERSION` is node version, like `14` - switches which version of node you're using)
19.    `nvm install NEW_VERSION --reinstall-packages-from=OLD_VERSION` (helps install the latest LTS release without losing your last batch of stuff)
20.    `nvm alias default VERSION` (tells your computer what default node to use)
21.    `xcrun simctl list devices` (which xcode devices are available on your mac - requires full xcode to be installed)

## Expo / React Native

To clear cache, as of Expo SDK v42.0.0 on MacOS 11.5.2 (Big Sur):

1. `rm -rf node_modules` (dumps node_modules)
2. `yarn cache clean` (runs cache cleaner for yarn)
3. `yarn` (reinstalls deps)
4. `watchman watch-del-all` (kills cache in live updated watchman)
5. `rm -fr $TMPDIR/haste-map-*` (to be honest, I'm not really sure)
6. `rm -rf $TMPDIR/metro-cache` (works to clear metro builder cache)
7. `expo start --clear` (restarts expo server and clears it's cache - `.expo` folder in your file explorer)
