## Client users connection to personicle


- **Allow your users to connect their personicle**
  - The following link allows user to sign in to their personicle
    -
     ```
      https://dev-01936861.okta.com/oauth2/aus445eqrgaj1kKdh5d7/v1/authorize?client_id=your_client_id&redirect_uri=your_redirect_uri&response_type=token&scope=openid+profile+email+additional_scopes&state=anyRandomString&nonce=anyRandomString 
    ```
    - [List of all scopes](https://github.com/tirth-clearsense/Personicle/blob/client-registration-doc/docs/scopes.md)
    -  Include the scopes that you want to accees in the above url in scopes parameter. Example: ``` scope=openid+profile+email+com.personicle.individual.datastreams.heartrate+events.read ```. Scopes can be updated [here](https://personicle-client-registration.herokuapp.com/update-scopes).
    -  After successful sign in, the access token will be present in the redirect uri that was specified earlier.
    
 - **Make request to personicle for data access**
    - Events endpoint
      - ``` https://20.121.8.101:3000/request/events ```
      - Parameters: startTime, endTime, source (optional, example: google-fit), event_type(optional, example: sleep)
      - Headers: Authorization: access token
      
    - Datastreams endpoint
      - ``` https://20.121.8.101:3000/request ```
      - Parameters: datatype (example: com.personicle.individual.datastreams.heartrate), startTime, endTime, source (optional, example: google-fit)
      - Headers: Authorization: access token
<!-- 
## Client users personicle connection

Allow users of client application to connect their personicle

- **Get personicle user access token**
    - Allow users to log in to their personicle account
      - Request Example for **implicit grant flow**: 
          ```
               https://dev-01936861.okta.com/oauth2/default/v1/authorize?client_id=your_client_id&redirect_uri=your_redirect_uri&response_type=token&scope=openid+profile+email&state=anyRandomString&nonce=anyRandomString
          ```

      - Response Example (If successful login): 
   
        ```
           Access token for the user will be present in the url. 
        ```
        
    - Request Example for **authorization grant flow**:
        ```
        https://dev-01936861.okta.com/oauth2/default/v1/authorize?client_id=your_client_id&redirect_uri=your_redirect_uri&response_type=code&scope=openid+profile+email&state=anyRandomString&nonce=anyRandomString
        ```
     - Response Example (If successful login): 

    ```
       Code will be returned in your redirect url. You'll need to exchange this code for access and id tokens. See below.
    ```
        
- **Get Access token (For authorization code flow)**
    
    - Request Example:
        ```
            curl -v -X POST \
            -H "Content-type:application/x-www-form-urlencoded" \
            "https://dev-01936861.okta.com/oauth2/default/v1/token" \
            -d "client_id=your_client_id&client_secret=your_client_secret&grant_type=authorization_code&redirect_uri=your_redirect_uri&code=code_returned_from_previous_step"
        ```
        
     - Response Example:
        ```
        {"token_type":"Bearer","expires_in":3600,"access_token":"user_access_token","scope":"openid profile email","id_token":"user_id_token"}
        
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

 -->
