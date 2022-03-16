## Client Registration to Personicle

Client registration API for access to personicle data.

- **Register your application**

  - Request Example: 
      ``` 
      curl -v -X POST -H "Accept: application/json" -H "Content-Type: application/json" -H "Authorization: SSWS 00yx92A2rwfRM-JCLookK04GgaNKNtVhNeD5-ONF8N" -d '{
        "client_name": "Your application name",
        "client_uri": "Your application uri",
        "application_type": "service",
        "response_types": [
           "token"
        ],
         "grant_types": [
          "client_credentials"
        ],
        "token_endpoint_auth_method": "client_secret_basic"
      }' "https://dev-01936861.okta.com/oauth2/v1/clients"
      ```

Response Example: 
``` 
{"client_id":"your_client_id","client_secret":"your_client_secret","client_id_issued_at":1647470465,"client_secret_expires_at":0,"client_name":" Your application name ","client_uri":"your application uri","logo_uri":null,"redirect_uris":[],"response_types":["token"],"grant_types":["client_credentials"],"token_endpoint_auth_method":"client_secret_basic","application_type":"service"}
```

