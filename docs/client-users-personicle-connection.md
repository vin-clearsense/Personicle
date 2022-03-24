
## Client users personicle connection

Allow users of client application to connect their personicle

- **Get personicle user access token**
    - Allow users to log in to their personicle account
      - Request Example: 
          ```
               https://dev-01936861.okta.com/oauth2/default/v1/authorize?client_id=your_client_id&redirect_uri=your_redirect_uri&response_type=token&scope=openid+profile+email&state=anyRandomString&nonce=anyRandomString
          ```

      - Response Example (If successful login): 
   
        ```
           Access token for the user will be present in the url. 
        ```
- **Get personicle user id**
    - Request Example:
      ```
        curl -X GET \
        -H "Authorization: Bearer {access_token}" \
       "https://dev-01936861.okta.com/oauth2/default/v1/userinfo"
      ```
      
    - Response Example:
       ```
       {"sub":"user_id","name":"user_name","locale":"en_US","email":"user_email","preferred_username":"","given_name":"","family_name":"","zoneinfo":"America/Los_Angeles","updated_at":1648137830,"email_verified":true}
       ```
- **Call Personicle api with user accesstoken and user id retrieved from previous step**
   - 

