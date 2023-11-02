# Shop_API_Test_Report

## How to run this project
- Clone this project
- Open with Postman / Command Shell
- Run Command:  
```console 
newman run Shop_API_Manan_Ahmed_Broti.postman_collection.json -e Shop_API_Manan_Ahmed_Broti.postman_environment.json
```
- Run Command for Report: 
```console 
newman run Shop_API_Manan_Ahmed_Broti.postman_collection.json -e Shop_API_Manan_Ahmed_Broti.postman_environment.json -r cli,htmlextra
```
- Run Command for Report With Iteration: 
```console 
newman run Shop_API_Manan_Ahmed_Broti.postman_collection.json -e Shop_API_Manan_Ahmed_Broti.postman_environment.json -n "number of iteration" -r cli,htmlextra
```

## Technology used:
- Postman
- Newman

## Prerequisite:
- Jdk
- Node Js
- Newman
- Html Report Library

## Newman and Report Installation Process:
- Newman Install Command:
```console
npm install -g newman
```
- Newman Html Report Install Command:
```console
npm install -g newman-reporter-htmlextra
```
## API Live Report:
- https://shop-api.ahmedmanan.com/report

## API Documentation:
- [https://documenter.getpostman.com/view/13082503/2s93Xwz4Az](https://documenter.getpostman.com/view/23708981/2s9YRGy9ao)

## Newman Report Summary:
![Test Summary](summary.png)

Total Number of Test Scripts 78 and a Total of 237 Assertions were done. All of them passed with 0 skipped tests. The number of iterations is 3.

## Test case list & Test Features:
1. ### Registration
   - &check; Create data sets using the dynamic random variables.
   - &check; Generate authentication token
   - &check; Check status code
   - &check; Store the dataset in the environment

2. ### Login
	In the test I have validated the following field values & checked those features:
 	- &check; Email
 	- &check; Password
 	- &check; Generate token
 	- &check; Check status code
3. ### Create A Product
	In the test I have validated the following field values & checked those features:
 	- &check; Create data sets using dynamic random variables
	- &check; Check status code
 	- &check; Product price validation
 	- &check; Product quantity validation
 	- &check; Product name validation
	- &check; Store dataset in the environment
 3. ### Get all Products
	In the test I have validated the following field values & checked those features:
     	- &check; Check status code 
 	- &check; Check the product ID found in the list
 	- &check; Check the product name found in the list
 	- &check; Check the product description found in the list
	- &check; Check the product category found in the list
   	- &check; Check the product quantity found in the list
    	<li>&check; Check the product price found in the list</li>
     	<li>&check; Check the product picture found in the list</li>
