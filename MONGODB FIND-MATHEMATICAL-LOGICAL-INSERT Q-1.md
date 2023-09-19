show dbs
use unit2
show collections

Find a document with the first name 'Danit' from the collection.
--db.Employees.find({name:"Danit"})

Fetch all documents where the age is greater than or equal to 30.
--db.Employees.find({age:{$gte:30}})

Retrieve all documents where the salary is less than or equal to 70000
--db.Employees.find({salary:{$lte:70000}})

Find all documents where the age is greater than 30 and the salary is less than 90000.
--db.Employees.find({salary:{$lt:90000},age:{$gt:30}})

Retrieve all documents where the gender is 'Female' and the age is less than 25.
--db.Employees.find({gender:'Female',age:{$lt:25}})

Find all documents where the last name is 'Bestall' or the salary is greater than 80000.
--db.Employees.find({$or:[{last_name:"Bestall"},{salary:{$gt:80000}}]})

Retrieve all documents where the gender is 'Male' and (age is less than 25 or salary is greater than 80000).
--db.Employees.find({gender:'Male',$or:[{age:{$lt:25}},{salary:{$gt:80000}}]})

Add a new student named 'Bob' with a last name 'Smith', male gender, age 22, and a salary of 60000 to the collection
--db.Employees.insertOne({firstName:'Bob',lastName:'Smith',gender:'Male',age:22,salary:60000})

Retrieve all documents where the gender is 'Male' and age is greater than 40
--db.Employees.find({$and:[{gender:'Male'},{age:{$gt:40}}]})

Find all documents where the last name is not 'Bestall' or the salary is less than 80000
--db.Employees.find({$or:[{last_name:'Bestall'},{salary:{$lt:80000}}]})