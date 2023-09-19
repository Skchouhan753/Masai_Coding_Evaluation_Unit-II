1. Write a MongoDB query to find all documents where "Swimming" is one of the hobbies.
-- db.users.find({"hobbies":"Swimming"})

2. Write a MongoDB query to find all documents where "Reading" or "Gaming" is one of the hobbies
-- db.users.find({$or:[{"hobbies":"Swimming"},{"hobbies":"Reading"}]})

3. Write a MongoDB query to find all documents where "Hiking" or "Photography" is one of the hobbies.
-- db.users.find({$or:[{"hobbies":"Hiking"},{"hobbies":"Photography"}]})

4. Write a MongoDB query to find all documents where the "state" field within the "address" object is equal to "CA."
-- db.users.find({"address.state":"CA"})

5. Write a MongoDB query to find all documents where the "city" field within the "address" object is not equal to "New York."
-- db.users.find({"address.city":{$ne:"New York"}})

6. Write a MongoDB query to find all documents where the "zipcode" field within the "address" object is not equal to "54321."
-- db.users.find({"address.zipcode":{$ne:"54321"}})

7. Write a MongoDB query to find all documents where the "street" field within the "address" object contains the word "Main."
-- db.users.find({"address.street":"Main"})

8. Write a MongoDB query to find all documents where the "region" field within the "address" object exists.
-- db.users.find({"address.region":{$exists:true}})

9. Write a MongoDB query to find all documents where the sum of expenses is greater than or equal to 1500.
-- db.users.aggregate([{$match:{$expr:{$gte:[{$sum:"$expenses"},1500]}}}])
-- db.users.find({$expr:{$gte:[{$sum:"$expenses"},1500]}})

10. Write a MongoDB query to find all documents where the average (mean) of expenses is less than 300.
-- db.users.find({$expr:{$lt:[{$avg:"$expenses"},300]}})

11. Write a MongoDB query to find all documents where the maximum expense is greater than or equal to 400.
-- db.users.find({$expr:{$gte:[{$max:"$expenses"},400]}})

12. Write a MongoDB query to find all documents where the minimum expense is less than 200. d
-- db.users.find({$expr:{$lt:[{$max:"$expenses"},200]}})

13. Write a MongoDB query to find all documents where the sum of "zipcode" values within the "address" object is greater than or equal to 50000.
-- db.users.aggregate([{$project:{totalZipcode:{$sum:"$address.zipcode"}}},
{$match:{totalZipcode:{$gte:50000}}}])

14. Write a MongoDB query to find all documents where the average of "zipcode" values within the "address" object is less than 30000.
-- db.users.find({$expr:{$lt:[{$avg:"$address.zipcode"},30000]}})

15. Write a MongoDB query to find all documents where the maximum "zipcode" value within the "address" object is greater than or equal to 40000.
--

16. Write a MongoDB query to find all documents where the minimum "zipcode" value within the "address" object is less than 20000.
--

17. Write a MongoDB update query to push a new hobby "Swimming" into the "hobbies" array for the document where "name" is "Alice.
-- db.sers.updateOne({name:"Alice"},{$push:{hobbies:"Swimming"}})

18. Write a MongoDB update query to push a new hobby "Hiking" into the "hobbies" array for the document where "name" is "Boby".
-- db.users.updateOne({name:"Boby"},{$push:{hobbies:"Hiking"}})

19. Write a MongoDB update query to push a new hobby "Dancing" into the "hobbies" array for the document where "name" is "Carol".
-- db.users.updateOne({name:"Carol"},{$push:{hobbies:"dancing"}})

20. Write a MongoDB update query to pop the last hobby from the "hobbies" array for the document where "name" is "David."
-- db.users.updateOne({name:"David"},{$pop:{hobbies:1}})

21. Write a MongoDB update query to pop the first hobby from the "hobbies" array for the document where "name" is "Hank."
-- db.users.updateOne({name:"Hank"},{$pop:{hobbies:-1}})

22. Write a MongoDB update query to pop the hobby "Coding" from the "hobbies" array for the document where "name" is "Francis."
-- db.users.updateOne({name:"Francis"},{$pull:{hobbies:"Coding"}})

23. Write a MongoDB update query to change the value at index 1 of the "hobbies" array to "Cooking" for the document where "name" is "Alice."
-- db.users.updateOne({name:"Alice"},{$set:{"hobbies.1":"Cooking"}})

24. Write a MongoDB update query to change the value at index 0 of the "hobbies" array to "Soccer" for the document where "name" is "Hank."
-- db.users.updateOne({name:"Hank"},{$set:{"hobbies.0":"Soccer"}})

25. Write a MongoDB update query to change the value at index 2 of the "hobbies" array to "Gaming" for the document where "name" is "David."
-- db.users.updateOne({name:"David"},{$set:{"hobbies.2":"Gamming"}})
 
26. Write a MongoDB update query to add a new key-value pair "country: USA" to the "address" object for the document where "name" is "Alice."
-- db.users.updateOne({name:"Alice"},{$set:{"address.country":"USA"}})

27. Write a MongoDB update query to add a new key-value pair "postalCode: 54321" to the "address" object for the document where "name" is "David."
-- db.users.updateOne({name:"David"},{$set:{"address.postalCode":54321}})

28. Write a MongoDB update query to add a new key-value pair "region: West" to the "address" object for the document where "name" is "Eva."
-- db.users.updateOne({name:"E"},{$set:{"address.region":"West"}})

29. Write a MongoDB update query to change the value of the "state" field in the "address" object to "MA" for the document where "name" is "Alice."
-- db.users.updateOne({name:"Alice"},{$set:{"address.state":"MA"}})

30. Write a MongoDB update query to change the value of the "zipcode" field in the "address" object to "54321" for the document where "name" is "David."
-- db.users.updateOne({name:"David"},{$set:{"address.zipcode":54321}})

31. Write a MongoDB update query to change the value of the "city" field in the "address" object to "Techville" for the document where "name" is "Eva."
-- db.users.updateOne({name:"Eva"},{$set:{"address.city":"Techville"}})

32. Write a MongoDB update query to change the value of the "city" field in the "address" object to "New City" for the document where "name" is "Francis.
-- db.users.updateOne({name:"Francis"},{$set:{"address.city":"New City"}})