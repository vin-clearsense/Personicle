## Client users connection to personicle


- **Allow your users to connect their personicle**
  - The following link allows user to sign in to their personicle
    -
     ```
      https://dev-01936861.okta.com/oauth2/aus445eqrgaj1kKdh5d7/v1/authorize?client_id=your_client_id&redirect_uri=your_redirect_uri&response_type=token&scope=openid+profile+email+additional_scopes&state=anyRandomString&nonce=anyRandomString 
    ```
    - [List of all scopes](https://github.com/tirth-clearsense/Personicle/blob/client-registration-doc/docs/scopes.md)
    -  Access your application scopes [here](https://personicle-client-registration.herokuapp.com/get-scopes)
    -  Include the scopes that you want to accees in the above url in scopes parameter. Example: ``` scope=openid+profile+email+com.personicle.individual.datastreams.heartrate+events.read ```. 
    -  Scopes can be updated [here](https://personicle-client-registration.herokuapp.com/update-scopes). **Note: ** This will override your current scopes.
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

