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