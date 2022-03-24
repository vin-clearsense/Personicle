## Client Registration to Personicle

Client registration API for access to personicle data.

- **Register your application**

  - Request Example: 
      ``` 
       curl -v -X POST \
      -H "Accept: application/json" \
      -H "Content-Type: application/json" \
      -H "Authorization: SSWS 00yx92A2rwfRM-JCLookK04GgaNKNtVhNeD5-ONF8N" \
      -d '{
        "client_name": "Your client app name",
        "client_uri": "{Your client uri, example: http://localhost:3000}",
        "application_type": "web",
        "redirect_uris": [
           "{your redirect uri, example: http://localhost:3000/callback}"
        ],
        "post_logout_redirect_uris": [
          " {your logout redrect uri, example: http://localhost:3000/oauth/callback/postLogoutRedirectUri}"
        ],
        "response_types": [
           "code",
           "id_token",
           "token"
        ],
        "grant_types": [
           "authorization_code",
           "refresh_token",
           "implicit",
           "client_credentials"
        ],
        "token_endpoint_auth_method": "client_secret_basic",
        "initiate_login_uri": " {your login uri, example: https://www.example-application.com/oauth2/login}"
      }' "https://dev-01936861.okta.com/oauth2/v1/clients"
      ```

  - Response Example: 
      ``` 
    {"client_id":"your client id","client_secret":"your client secret","client_id_issued_at":1648137003,"client_secret_expires_at":0,"client_name":"Your client app   name","client_uri":"http://localhost:3000","logo_uri":null,"redirect_uris":["http://localhost:3000"],"post_logout_redirect_uris":["http://localhost:3000/oauth/callback/postLogoutRedirectUri"],"response_types":["code","id_token","token"],"grant_types":["authorization_code","refresh_token","implicit","client_credentials"],"initiate_login_uri":"https://www.example-application.com/oauth2/login","token_endpoint_auth_method":"client_secret_basic","application_type":"web"}
      ```
      
      
- **Assign users to your application**
    - Request Example:
      ```
          curl -v -X PUT \
    -H "Accept: application/json" \
    -H "Content-Type: application/json" \
    -H "Authorization: SSWS 00yx92A2rwfRM-JCLookK04GgaNKNtVhNeD5-ONF8N" \
    -d '{
    }' "https://dev-01936861.okta.com/api/v1/apps/{your_client_id}/groups/00g3sfiuiukeC6Mj75d7"
      ```
      
   - Response Example:
      ```
      {"id":"00g3sfiuiukeC6Mj75d7","lastUpdated":"2022-03-24T16:03:50.000Z","priority":0,"profile":{},"_links":{"app":{"href":"https://dev-01936861.okta.com/api/v1/apps/{your_client_id}"},"self":{"href":"https://dev-01936861.okta.com/api/v1/apps/{your_client_id}/groups/00g3sfiuiukeC6Mj75d7"},"group":{"href":"https://dev-01936861.okta.com/api/v1/groups/00g3sfiuiukeC6Mj75d7"}}}
      ```
<!-- - **Encode your clientId and clientSecret to base64 encoded string**
   - Example conversion for macOS/Linux
      - Run the following command replacing ```clientId``` and ```clientSecret``` with your clientId and clientSecret:
      
         ``` echo -n clientId:clientSecret | base64 ```
      - Include the returned string as Authorization header in the next step
   
- **Obtain access token**
    - Request Example:
      ```
        curl -v -X POST \
        -H "Content-type:application/x-www-form-urlencoded" \
        -H "Authorization:Basic ${Base64(<client_id>:<client_secret>)}" \
        "https://dev-01936861.okta.com/oauth2/default/v1/token" \
        -d "grant_type=client_credentials&scope=dataapi"
      ```
    - Response Example:
      ```
        {"token_type":"Bearer","expires_in":3600,"access_token":"Your access token","scope":"dataapi"}
      ```
- **Make request to personicle api with access token as Authorization header** -->
