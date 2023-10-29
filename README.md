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
    1. > Create Data Sets Using the Dynamic Random Variables.
    2. > Generate authentication token
    3. > Check status code
    4. > Store dataset in the environment

3. ### Login
	> In the test I have validated the following field values & checked those features:
 	1. > Email
 	2. > Password
 	3. > Generate Token
 	4. > Check status code
