1. Retrieve documents where the age is either 30 or 35.
--db.Employees.find({$or:[{age:30},{age:40}]})

2. Find all documents where the gender is not 'Male' and age is greater than 25
--db.Employees.find({$and:[{gender:{$ne:'Male'}},{age:{$gt:25}}]})

3. Retrieve documents where the age is less than 30 and the last name is 'Bestall'
--db.Employees.find({$and:[{age:{$lt:30}},{lastName:'Bestall'}]})

4. Find all documents where the gender is 'Female' and (age is less than 25 or salary is greater than 90000).
--db.Employees.find({$and:[{age:"Female"},{$or:[{age:{$lt:25}},{salary:{$gt:90000}}]}]})
                                      ----OR---
--db.Employees.find({ gender:'Female',$or:[{age:{$lt:25}},{salary:{$gt:90000}}]})

5. Retrieve documents where the age is not equal to 36.
--db.Employees.find({age:{$ne:36}})

6. Find all documents where the gender is 'Male' and salary is less than or equal to 70000
--db.Employees.find({$and:[{gender:"Male"},{salary:{$lte:70000}}]})

7. Retrieve documents where the age is greater than or equal to 30 and the last name is not 'Bestall'
--db.Employees.find({$and:[{age:{$gte:30}},{last_name:{%ne:"Bestall"}}]})

8. Find all documents where the gender is 'Female' and (age is greater than 40 or salary is less than 80000).
--db.Employees.find({$and:[{gender:"Female"},{$or:[{age:{$gt:40}},{salary:{$lt:80000}}]}]})
                                        ---OR---
--db.collectionName.find({gender:'Female',$or:[{age:{$gt:40}},{salary:{$lt:80000}}]})

9. Retrieve all documents where the salary is greater than 100000.
--db.Employees.find({salary:{$gt:100000}})

10. Find all documents where the age is equal to 30.
--db.Employees.find({age:30})

11. Retrieve documents where the salary is less than 75000.
--db.Employees.find({salary:{$lt:75000}})

12. Find all documents where the age is less than 35 and the salary is greater than or equal to 80000.
--db.Employees.find({$and:[{age:{$lt:35}},{salary:{$gte:80000}}]})

13. Retrieve documents where the salary is not equal to 92611.
--db.Employees.find({salary:{$ne:92611}})

14. Find all documents where the age is greater than 25 and the salary is less than 70000.
--db.Employees.find({age:{$gt:25},{salary:{$lt:70000}}})

15. Retrieve documents where the age is equal to 36 and the salary is greater than 90000.
--db.Employees.find({$and:[{age:36},{salary:{$gt:90000}}]})

16. Find all documents where the salary is less than 80000 and age is not equal to 22.
--db.Employees.find({$and:[{age:{$ne:22}},{salary:{$lt:80000}}]})

17. Retrieve documents where the age is less than 40 and the salary is greater than 60000.
--db.Employees.find({$and:[{age:{$th:40}},{salary:{$gt:60000}}]})

18. Find all documents where the salary is equal to 75000.
--db.Employees.find({salary:75000})

19. Retrieve documents where the gender is 'Male' and (age is less than 30 or salary is greater than 80000).
--db.Employees.find({gender:"Male",{$or:[{age:{$lt:30}},{salary:{$gt;80000}}]}})

20. Find all documents where the age is greater than 35 and (gender is 'Female' or salary is less than 90000).
--db.Employees.find({$and:[{age:{$gt:35}},{$or:[{gender:"Female"},{salary:{$lt:90000}}]}]})

21. Retrieve documents where the gender is 'Male' and age is less than 25 or (last name is 'Bestall' and salary is greater than 80000).
--db.Employees.find({$and:[{gender:"Male"},{age:{$lt:25}},{$or:[{last_name:"Bestall"},{salary:{$gt:80000}}]}]})

22. Find all documents where the age is not equal to 36 and (gender is 'Female' or salary is less than 70000).
--db.Employees.find({$and:[{age:{$ne:36}},{$or:[{gender:'Female'},{salary:{$lt:70000}}]}]})

23. Retrieve documents where the age is greater than 30 or (gender is 'Male' and salary is less than 75000).
--db.Employees.find({$or:[{age:{$gt:30}},{$and:[{gender:"Male"},{salary:{$lt:75000}}]}]})

24. Find all documents where the salary is less than or equal to 70000 and (gender is 'Male' or age is greater than 40).
--db.Employees.find({salary:{$lte:700000},{$or:[{gender:"Male"},{age:{$gt:40}}]}})

25. Retrieve documents where the age is less than 35 and (gender is 'Female' and salary is greater than 80000).
--db.Employees.find({$and:[{age:{$lt:35}},{gender:"female"},{salary:{$gt:80000}}}]})
                                ---OR---
--db.Employees.find({age:{$lt:35},$and:[{gender:'Female'},{salary:{$gt:80000}}]})


26. Find all documents where the gender is not 'Male' and age is greater than 25 or (salary is less than 60000 and last name is 'Smith').
--db.Employees.find({$or:[{gender:{$ne:'Male'},age:{$gt:25}},{salary:{$lt:60000},last_name:'Smith'}]})

27. Retrieve documents where the age is equal to 22 and (gender is 'Female' or salary is greater than 70000).
--db.Employees.find({$and:[{age:22},{$or:[{gender:"Female"},{salary:{$gt:70000}}]}]})

28. Find all documents where the salary is not equal to 92611 and (gender is 'Male' or age is less than 30).
--db.Employees.find({$and:[{salary:{$ne:92611}},{$or:[{gender:"Male"},{age:{$lt:30}}]}]})
