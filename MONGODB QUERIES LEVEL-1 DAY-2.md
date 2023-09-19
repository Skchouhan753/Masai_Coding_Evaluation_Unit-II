1. Update the salary of Kimbra Ballentime to $55,000

-- db.Employees.updateOne({"first_name":"Kimbra","last_name":"Ballentime"},{$set:{"salary":55000}})

2. Update the gender of Alla Spehr to 'Male'

-- db.Employees.updateOne({"first_name":"Alla","last_name":"Spher"},{$set:{"gender":"Male"}})

3. Update the age of Bennie Doerr to 20 years old

-- db.Employees.updateOne({"first_name":"Bennie","last_name":"Doerr"},{$set:{"age":20}})

4. Increase the salary of all male employees under the age of 40 by 10%:

-- db.Employees.update({"gender":"Male","age":{$lt:40}},{$mul:{"salary":0.1}})

5. Update the last name of employees with the last name 'Sartain' to 'Smith'

-- db.Employees.update({"last_name":"Sartain"},{$set:{"last_name":"Smith"}})

6. Change the gender of all employees with a salary less than $40,000 to 'Other'

-- db.Employees.update({"salary":{$lt:40000}},{$set:{"gender":"Other"}})

7. Increase the salary of all employees by 5%

-- db.Employees.update({},{$mul:[{"salary":1.05}]})

8. Increase the salary of male employees by 8% and female employees by 6%

--

9. Update the salary of employees who are 30 years old by 15%, 40 years old by 10%, and 50 years old by 5%

--

10. Delete the employee with the first name 'Bennie' and last name 'Doerr'

-- db.Employees.deleteOne({"first_name":"Bennie","last_name":"Doerr"})

11. Delete all employees with a salary less than $30,000

-- db.Employees.delete({"salary":{$lt:30000}})

12. Delete all male employees under the age of 40

-- db.Employees.delete({"gender":"Male","age":{$lt:40}})