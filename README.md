# Mongodb-Handson1
https://prepbytes-misc-images.s3.ap-south-1.amazonaws.com/assets/1640781204638-employee.json

## Do all the above queries using Mongo Shell.

### Q1. Create a database , give it name like "Human_Resource". Create a collection inside this named "employee".
#### To create new Database
      -> use Human_Resource 
#### To select the Database
      -> switched to db Human_Resource
#### To create collection and insert One data inside the collection
      -> db.employee.insertOne({"firstName": "John","lastName": "Doe", "salary": "25000","department": "HR","lastCompany": "X","lastSalary": "10000","overallExp": "2","contactInfo": "1234567890","yearGrad": "2016","gradStream": "CSE"})

#### To insert multiple data inside the collection
      -> db.employee.insertMany([{"firstName": "Rohan", "lastName": "Jame", "salary": "30000", "department": "Technical", "lastCompany": "Y", "lastSalary": "15000", "overallExp": "1", "contactInfo": "1234567860", "yearGrad": "2015", "gradStream": "CSE"},{"firstName": "Jame", "lastName": "Doe", "salary": "35000", "department": "Accounts", "lastCompany": "Z", "lastSalary": "20000", "overallExp": "1", "contactInfo": "123567890", "yearGrad": "2019", "gradStream": "ECE"},{"firstName": "Sao", "lastName": "Avika", "salary": "30000", "department": "Sales", "lastCompany": "Y", "lastSalary": "15000", "overallExp": "2", "contactInfo": "1234567860", "yearGrad": "2015", "gradStream": "CSE"},{"firstName": "Jame", "lastName": "roh", "salary": "35000", "department": "Accounts", "lastCompany": "Z", "lastSalary": "15000", "overallExp": "2", "contactInfo": "123567890", "yearGrad": "2019", "gradStream": "EEE"}, {"firstName": "Rohan", "lastName": "Jame", "salary": "30000", "department": "Technical", "lastCompany": "Y", "lastSalary": "15000", "overallExp": "1", "contactInfo": "1234567860", "yearGrad": "2015", "gradStream": "CSE"},{"firstName": "Jame", "lastName": "Doe", "salary": "35000", "department": "Accounts", "lastCompany": "Z", "lastSalary": "20000", "overallExp": "1", "contactInfo": "123567890", "yearGrad": "2019", "gradStream": "ECE"},{"firstName": "Sao", "lastName": "Avika", "salary": "30000", "department": "Sales", "lastCompany": "Y", "lastSalary": "15000", "overallExp": "2", "contactInfo": "1234567860", "yearGrad": "2015", "gradStream": "CSE"},{"firstName": "Jame", "lastName": "Doe", "salary": "35000", "department": "Accounts", "lastCompany": "Z", "lastSalary": "15000", "overallExp": "2", "contactInfo": "123567890", "yearGrad": "2019", "gradStream": "EEE"},{"firstName": "Rohan", "lastName": "Jame", "salary": "30000", "department": "Technical", "lastCompany": "Y", "lastSalary": "15000", "overallExp": "1", "contactInfo": "1234567860", "yearGrad": "2015", "gradStream": "CSE"},{"firstName": "Jame", "lastName": "Doe", "salary": "35000", "department": "Accounts", "lastCompany": "Z", "lastSalary": "20000", "overallExp": "1", "contactInfo": "123567890", "yearGrad": "2019", "gradStream": "ECE"},{"firstName": "Sao", "lastName": "Avika", "salary": "30000", "department": "Sales", "lastCompany": "Y", "lastSalary": "15000", "overallExp": "2", "contactInfo": "1234567860", "yearGrad": "2015", "gradStream": "CSE"},{"firstName": "Jame", "lastName": "Doe", "salary": "35000", "department": "Accounts", "lastCompany": "Z", "lastSalary": "15000", "overallExp": "2", "contactInfo": "123567890", "yearGrad": "2019", "gradStream": "EEE"}])



### Q2. Query the collection "employee" and list all the documents.
    -> db.employee.find()

### Q3. Query the collection "employee" and list the employees who are having salary more than 30000.
    -> db.employee.find({"salary":{$gt:"30000"}})
### Q4. Query the collection "employee" and list the employees who are having experience more than 2 years.
    -> db.employee.find({"overallExp":{$gte:"2"}})
### Q5. Query the collection "employee" and list the employees who are graduated after 2015 and having experience more than 1 year.
    -> db.employee.find({"yearGrad":{$gt:"2015"},"overallExp":{$gt:"1"}})
### Q6. Query the collection "employee" and update the salary of the employee whose salary is greater than 70000 to 65000.
    -> db.employee.updateMany({salary:{$gt:"70000"}},{$set:{salary:"65000"}})
### Q7. Delete all the documents from "employee" where last company is Y.
    ->db.employee.deleteMany({lastCompany:"Y"})
