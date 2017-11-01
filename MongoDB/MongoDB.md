# MongoDB Notes


## Start Mongo

In two different command prompts with admin access open the following files 

c:/mongodb/bin/mongod.exe

c:/mongodb/bin/mongo.exe


## Stop Mongo

use admin
db.shutdownServer() //watchout, this will shutdown the server!!!

# Basic Commands

use   //use a specific dbs
show dbs  // shows the dbs available 
show collections  //shows the collections in a specific DB

# Examples
use testdb
s = {Name : "bob"}  //data
db.testdb.insert(s) //inserts s in testdb. This creates the collection testdb. You can't have empty collections 

