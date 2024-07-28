
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
  - Action: Request sensitive information	
### Sample Payload
```json
{
  "client_id": "c16EJo48lbTCQEhqSztGGlmxxxmZ4z27",
  "email": "testingforvulns2@gmail.com",
  "password": "hacked123",
  "connection": "Username-Password-Authentication"
}
```

## Perfect write-up's to read

 - [Authentication bypass in Auth0](https://sentorsecurity.com/blog/vulnerability-disclosure-authentication-bypass-in-auth0/)
 - [Authentication bypass in Auth0 via signup endpoint](https://naumankh4n.medium.com/a-click-can-cause-1600-auth0-misconfig-9234aedad55c)
