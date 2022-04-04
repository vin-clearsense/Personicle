## Client Registration to Personicle

Client registration for access to personicle data.

- **Register your application**

  - Go to [Personicle client registration](https://personicle-client-registration.herokuapp.com/register) to register your app.

  - Fill in your application name, application uri (example:https://example.com), redirect uri (example: https://example.com/callback) and select the scopes that your  app needs access to from personicle. Click Register.
  
  - After successful registration, your **client id** and **client secret** will be generated. Make sure to make a note of it. You won't have access to them later.

- **Allow your users to connect their personicle**
  - The following link allows user to sign in to their personicle
    -
     ```
      https://dev-01936861.okta.com/oauth2/aus445eqrgaj1kKdh5d7/v1/authorize?client_id=your_client_id&redirect_uri=your_redirect_uri&response_type=token&scope=openid+profile+email+additional_scopes&state=anyRandomString&nonce=anyRandomString 
    ```
    -  Include the scopes that you want to accees in the above url in scopes parameter. Example: ``` scope=openid+profile+email+com.personicle.individual.datastreams.heartrate+events.read ```
    -  After successful sign in, the access token will be present in the redirect uri that was specified earlier.
 
 - **Make request to personcile for data access**
  
