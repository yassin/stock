# Project Stock

#### 1. Description 
this project is a (SpringBoot + mongoDB) Rest API

#### 2. Installation
##### install MongoDB 
install comunity server V4.0.0 https://www.mongodb.com/download-center#community
##### start mongoDB
shell 1 : ./<installDir>/bin/mongod --dbpath <path to new folder sb>
mongoDB is started

shell 2 : ./<installDir>/bin/mongo
use stock
db.createUser( { user: "stock-pharmacy-dev",
                 pwd: "stockpharmacy1dev",
                 roles: [ { role: "clusterAdmin", db: "admin" },{ role: "readAnyDatabase", db: "admin" },"readWrite"] },
               { w: "majority" , wtimeout: 5000 } )
 
#### Run API
spring-boot:run -Dspring.profiles.active=dev 

#### 3.Check API swagger
http://localhost:8080/swagger-ui.html
