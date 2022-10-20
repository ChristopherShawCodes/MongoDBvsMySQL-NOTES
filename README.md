# MongoDBvsMySQL-NOTES

Start server 

Command: mongosh
---------------------------

Exit server

Command: exit 

---------------------------

-------------------------------------------

run as a macOs service:

brew services start mongodb-community@5.0

stop:

brew services stop mongodb-community@5.0

-------------------------------------------


Comparing MongoDB to MySQL


Database Type:	                          
-------------------------------------------------------------------------------
Database

MySQL:

Schema	 


Mongo:

Database (db)

-------------------------------------------------------------------------------

Collection of related records	 

MySql:

Tables	  

Mongo:

Collections

-------------------------------------------------------------------------------

Each one record in the collection of records	

MySql:

Row / Record	

Mongo:

Document


****************** MySQL Database Schema == MongoDB Database (db) *****************

Database will be used to hold an entire project's Database


Commands: 
-------------------------------------------------


Show all databases available on our current MongoDB server	

Command:
show dbs
-------------------------------------------------

Show current database selected	
Command:
db

-------------------------------------------------

Change to another database
Note: If the database you're trying to switch to does not exist, 
Mongo shell will create a new database and switch to it.	

Pattern:
use DB_NAME

Command:
use message_board_db

-------------------------------------------------

Delete database
Note: db.dropDatabase() will delete the current database in use.

Command:
use message_board_db
db.dropDatabase()



****************** MySQL: Tables == MongoDB: Collections *****************

-------------------------------------------------


View all collections in a MongoDB	
Command:
show collections
-------------------------------------------------


Create a new collection in the current database	
Pattern:
db.createCollection("COLLECTION_NAME")

Command:
db.createCollection("ninjas")
-------------------------------------------------


Destroy a collection 	
Pattern:
db.COLLECTION_NAME.drop()

Command:
db.ninjas.drop()
-------------------------------------------------

****************** MySQL: Record == MongoDB: Document (BJSON Object) *****************


