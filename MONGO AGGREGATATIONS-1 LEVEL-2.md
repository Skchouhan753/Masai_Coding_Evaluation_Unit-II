Write Mongo query to retrieve the documents from the orders where the customer_id is 1.
-- db.orders.find({"customer_id":1})

Write Mongo query to retrieve documents from the products where supplier_id is 3 .
-- db.products.find({"supplier_id":3})

Write Mongo query to retrieve the documents from the orders collection with "status": "shipped" .
-- db.orders.find({"status":"shipped"})

Write Mongo query to retrieve the amount and paymentMethod from payments where the paymentMethod is not UPI.
-- db.payments.find({paymentMethod:{$ne:"UPI"}},{amount:1,paymentMethod: 1})

Write Mongo query to retrieve the paymentstatus where the amount is greater than 100.
-- db.payments.find({"amount":{$gt:100}},{"paymentstatus":1})

Write Mongo query to retrieve the shipper_id and price from the order_details where the price is greater than 2000.
-- db.orders.find({"price":{$gt:2000}},{"shipper_id":1,"order_details":1})

Write Mongo query to retrieve the customer_id and _id from the orders where the status is not shipped.
-- db.orders.find({"status":{$ne:"shipped"}},{"customer_id":1,"_id":1})

Write Mongo query to retrieve documents from the products where category_id is 1 without product _id.
-- db.products.find({"category_id":1},{"_id":0})

Write Mongo query to retrieve name,quantity from the products where price greater than 1500 .
-- db.products.find({"price":{$gt:1500}},{"name":1,"quantity":1})

Write Mongo query to retrieve the name from the shippers where the phone number is 1-800-742-5877.
-- db.shippers.find({"phone":1-800-742-577},{"name":1})

Write Mongo query to retrieve the city and phone of the suppliers where the suppliers name is Sony.
-- db.supplirs.find({"name":"Sony"},{"city":1,"phone":1})

Write Mongo query to retrieve the name of the suppliers where the city is Tokyo.
-- db.supplirs.find({"city":"Tokyo"},{"name":1})

Write Mongo query to find amount of payment made through "UPI" ?
-- db.payments.find({"paymentMethod":"UPI"},{"amount":1})

Write Mongo query to find buyers city as key name "city" who uses hotmail ?
-- db.buyers.aggregate([{$match:{"email":{$regex:/hotmail\.com$/i}}},{$project:{city:"$address.city"}}])MONGO AGGREGATIONS-2 LEVEL-2

Write Mongo query to find buyers name who from state "CA" ? (remove id also)
-- db.buyers.find({"address.city":"CA"},{"name":1})

Write Mongo query to find users with name and email who uses hotmail ?
<!-- -- db.buyers.find({"email":{$regex:/hotmail\.com$/i}},{"name":1,"email":1}) -->

Write Mongo query to find suppliers name and phone ?
-- db.supplirs.find({},{"name":1,"phone":1})

Write Mongo query to find buyers name,email, city and zip code ?
-- db.buyers.find({},{"name":1,"email":1,"address.city":1,"address.zip":1})

Write Mongo query to find buyers city and zip code ?
-- db.buyers.find({},{"address.city":1,"address.zip":1})

Write Mongo query to retrieve name,price from the products .
-- db.products.find({},{"name":1,"price":1})

Write Mongo query to retrieve the amount,paymentstatus and paymentMethod from payments.
-- db.payments.find({},{"amount":1,"paymentstatus":1,"paymentMethod":1})