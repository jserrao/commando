## Mongo (installed via Homebrew)

From: [https://stackoverflow.com/a/31165220/241153](https://stackoverflow.com/a/31165220/241153)

If using `homebrew`, and you should
- The databases are stored in the `/usr/local/var/mongodb/` directory
- The mongod.conf file is here: `/usr/local/etc/mongod.conf`
- The mongo logs can be found at `/usr/local/var/log/mongodb/`
- The mongo binaries are here: `/usr/local/Cellar/mongodb/[version]/bin`

If using without `homebrew`:
- The database lives at `/data/db`
- The mongod.conf files is here: `/usr/local/etc/mongod.conf`

01.    `mongod` (starts the mongo server from CLI)
02.    `brew services start mongo` (starts service from homebrew)
03.    `mongod --dbpath /your/path/here` (overrides where mongod wants to put it's data)
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
7.     `> db.collection.count()` (returns the number of records in a collection, argument is empty - it will just natively return the number)
8.     `> db.collection.find({ "key": "value" })` (finds a certain record by the key value, or a much bigger descriptive collection of records if need be, see example below)
```
db.restaurants.find(
  {
    "name": "The Coupe"
  }
)
```

9.   `> db.collection.update()  

```
db.your_collection.update(
  { criteria },
  {
    $set: { assignments }
  },
  { options }
)
```