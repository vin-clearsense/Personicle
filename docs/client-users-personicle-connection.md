
## Client users personicle connection

Allow users of client application to connect their personicle

- **Get personicle user id**
    - Allow users to log in to their personicle account
      - Request Example: 
          ``` 
             curl -v -X POST \
             -H "Accept: application/json" \
             -H "Content-Type: application/json" \
              -d '{
              "username": "test@example.com",
              "password": "password"
               }' "https://dev-01936861.okta.com/api/v1/authn"
          ```

  - Response Example (If successful login): 
  
        ``` 
   {"expiresAt":"2022-03-21T23:38:29.000Z","status":"SUCCESS","sessionToken":"20111hWiRn5z.....fw-hcL7OTja","_embedded":{"user": {"id":"00u3s...7","passwordChanged":"2022-02-03T17:38:23.000Z","profile":{"login":"test@example.com","firstName":"John","lastName":"Doe","locale":"en_US","timeZone":"America/Los_Angeles"}}},"_links":{"cancel":{"href":"https://dev-01936861.okta.com/api/v1/authn/cancel","hints":{"allow":["POST"]}}}}
        ```
  - Response Example (If invalid credentials):
      ```
      {"errorCode":"E0000004","errorSummary":"Authentication failed","errorLink":"E0000004","errorId":"oaevmSwdo6jSna9mLHeuctBow","errorCauses":[]}
      ```
- **Call Personicle api with user id retrieved from previous step**
   - 
   
- **Obtain access token**
    - 
