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
      

# Summery    
I have Completed effective API tests of a Product ordering site.   
https://shop-api.ahmedmanan.com/doc/     
<p align="center">
  <img src="" />
</p>
 

Here in this API new Products were ordered list of Products were viewed and different tests were performed like GET, POST, PUT, and DELETE.

**Summary:** Test Scripts 11 and a Total of 24 assertions were done. All of them passed with 0 skipped tests. The number of iterations is 1.



# Requirements   
**Postman**   
https://www.postman.com/   
**Node JS**   
https://nodejs.org/en/    

# Assertions Details    
#### Register User         
```bash
// set environment UserID
var jsonData = pm.response.json();
pm.environment.set("userID", jsonData.userID);

// environment Email and actual Email same or not
pm.test("Test Email", function () {
pm.expect(jsonData.email).to.eql(pm.environment.get("email"));
});

// Expected status code and response status code same or not
pm.test("Status code is 200", function () {
pm.response.to.have.status(200);
});     
```
#### Login    
```bash   
// set environment token
var jsonData = pm.response.json();
pm.environment.set("token", jsonData.token);


// environment token and actual token same or not
pm.test("Test Token", function () {
    pm.expect(jsonData.token).to.eql(pm.environment.get("token"));
});

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
