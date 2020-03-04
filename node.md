# Node (nvm, npm and yarn)

> Node.js is a runtime for JS that works outside your browser, one that you'll normally interact with via the CLI. By default it comes with `npm` which is node's package manager. You need to use npm to install both `nvm` (node version manager` and `yarn` (another jode.js package manager). To install those, you should generally use homebrew (`brew install yarn nvm`). In general, I prefer using nvm to manage node (instead of brew) and run packages with yarn (instead of npm). Brief background but hopefully that helps with these commands.

## node

01.    `node` (instantiates node runtime, drops you into a node interpreter - `> ` on the CLI indicates success)
02.    `> your-file-here.js` (tells node to run the file you put in there)
03.    `> .exit` (closes node runtime)

## nvm, node version manager

01.    `nvm install 12.5.1` (installs a specific version of node via nvm, node version manager)
02.    `nvm current` (tells you which version of node you're using)
03.    `nvm use 8` (tells nvm to switch your version of node, indicatd by the version number you type in)
04.    `nvm alias default 12.2.0` (makes 12.2.0 your default node version)

## npm, node package manager

01.    `npm install` (looks for a `package.json` file in your working directory, installs whatever packages you list there)
02.    `npm install package-here` (npm adds a package to your active project in `node_modules` folder AND `package.json`)
03.    `npm install --save package-here` (deprecated, as of NPM v5.x: [https://stackoverflow.com/a/19578808/241153](https://stackoverflow.com/a/19578808/241153))
04.    `npm uninstall package` (removes a package from package.json AND `node_modules` folder)

## yarn, another node package manager

01.    `yarn add package-here` (installs a package into `node_modules` and `package.json` dependency list)
02.    `yarn add -D package-here` (install a package as one of the `devDependencies` in `package.json`)
03.    `yarn install` (reads package.json file in your working directory and installs all the packages in there)
