
## Test for auth0 Tenants Misconfigurations

### Endpoints
- **Login Endpoint**:  
  `/usernamepassword/login`
  - Action: Try the login function

- **Signup Endpoint**:  
  `/dbconnections/signup`
  - Action: Signup with a new user
  - ***Sample Request***
    
  - ```request
    POST /dbconnections/signup HTTP/2
    Host: victim.auth0.com
    Origin: https://victim.auth0.com
    Referer: https://victim.auth0.com
    Content-Type: application/json
    Content-Length: 0

    {
      "client_id": "c16EJo48lbTCQEhqSztGGlmxxxmZ4z27",
      "email": "testingforvulns2@gmail.com",
      "password": "hacked123",
      "connection": "Username-Password-Authentication"
    }
    ```
- **Cross Origin Sharing Endpoint for auth**
  `/co/authenticate`
  - Action: In-progess	
### Sample Payload
```json
{
  "client_id": "c16EJo48lbTCQEhqSztGGlmxxxmZ4z27",
  "email": "testingforvulns2@gmail.com",
  "password": "hacked123",
  "connection": "Username-Password-Authentication"
}
```

--- 
