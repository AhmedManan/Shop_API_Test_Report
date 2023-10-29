# Shop_API_Test_Report
# Introduction
This document explains how to run API tests with Postman against restful APIs.    
# Content  
- [Summary](summary)      
- [Requirements](https://github.com/musthafiz/API-Testing#requirements)      
- [Assertions Details](assertions-details)   
  - [Register User](register-user)   
  - [Login](login)   
- [Create Test Suites](create-test-suites)      
      

# Summary    
I have Completed effective API tests of a Product ordering site.       
<p align="center">
https://shop-api.ahmedmanan.com/docs/   
</p>
 

Here in this API new Products were ordered list of Products were viewed and different tests were performed like GET, POST, PUT, and DELETE.

**Summary:** 
<p align="center">
  The Live Report Can be visited from here: https://shop-api.ahmedmanan.com/report/   
</p>
<p align="center">
     ![Test Summary](summary.png)
</p>
Total Number of Test Scripts 78 and a Total of 237 Assertions were done. All of them passed with 0 skipped tests. The number of iterations is 3.

# Requirements   
**Postman**   
https://www.postman.com/   
**Node JS**   
https://nodejs.org/en/    

# Assertions Details    
#### Register User         
```bash
var jsonData = pm.response.json()

// set environment token
pm.environment.set("token", jsonData.data.token)

// Expected status code and response status code same or not
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
```
#### Login    
```bash   
var jsonData = pm.response.json()

// set environment token
pm.environment.set("token", jsonData.data.token)

// environment name and actual name same or not
pm.test("Name Validation", function(){
    pm.expect(jsonData.data.user.name).to.equal(pm.environment.get("name"));
});

// environment email and actual email same or not
pm.test("Email Validation", function(){
    pm.expect(jsonData.data.user.name).to.equal(pm.environment.get("email"));
});

// Expected status code and response status code same or not
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
```
#### Create A Product    
```bash   
var jsonData = pm.response.json()

// environment name and response name same or not
pm.test("Name Validation", function(){
    pm.expect(jsonData.data.relationships.seller).to.equal(pm.environment.get("name"));
});


// Expected status code and response status code same or not
pm.test("Status code is 201", function () {
    pm.response.to.have.status(201);
});
```
#### Get All Products    
```bash   
// Expected status code and response status code same or not
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
```  

# Create Test Suites   

### Using Newman   


  Newman is a command-line Collection Runner for Postman. It enables you to run and test a Postman Collection directly from the command line.
#### Install Command    
```bash
npm install -g newman    
```
#### Run Command    
- newman run “Path/CollectionName.json” -e Path/EnvironmentName.json
- newman run “Collection Link” -e “Path”/EnvironmentName.json    

#### Create HTML Report  
 
#### Install Command      
```bash
npm install -g newman-reporter-html
```
**or**   
```bash
npm install -g newman-reporter-htmlextra    
```
#### Run Command      
- newman run “Collection Link” -e “Path”/EnvironmentName.json -r cli,html    
**or**    
- newman run “Collection Link” -e “Path”/EnvironmentName.json -r cli,htmlextra    
