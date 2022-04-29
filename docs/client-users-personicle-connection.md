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
    -  Scopes can be updated [here](https://personicle-client-registration.herokuapp.com/update-scopes). **Note:** This will override your current scopes.
    -  After successful sign in, the access token will be present in the redirect uri that was specified earlier.
    
 - **Make request to personicle for data access**
    - **Events endpoint**
      - Allows access to individual events within the soecified time range
      - ``` https://staging.personicle.org/data/read/request/events ```
      - Parameters: 
        - startTime: timestamp for the beginning of the required time interval e.g. 2022-01-04 15:54:12.092754, 
        - endTime: timestamp for the end of the required time interval e.g. 2022-01-08 15:54:12.092754, 
        - source: desired data source (optional, example: google-fit), 
        - event_type: desired event type(optional, example: sleep)
      - Headers: 
        - Authorization: Bearer `<access token>`
    - Request example  
      - ```
         GET https://staging.personicle.org/data/read/request/events?startTime=2022-01-04%2015:54:12.092754&endTime=2022-04-04%2010:54:12.092918 
        ```
    - Response example
      - ```
        [
          {
              "user_id": "003vx....121",
              "start_time": "2022-03-16T00:20:00",
              "end_time": "2022-03-16T00:40:00",
              "event_name": "Walking",
              "source": "google-fit",
              "parameters": {
                  "duration": 1200000,
                  "source_device": {
                      "packageName": "com.google.android.apps.fitness",
                      "version": "",
                      "detailsUrl": ""
                  }
              },
              "unique_event_id": "8821-12....c-b23h-00"
          }]    
          ```
    - **Datastreams endpoint**
      - ``` https://staging.personicle.org/data/read/request```
      - Parameters: datatype (example: com.personicle.individual.datastreams.heartrate), startTime, endTime, source (optional, example: google-fit)
      - Headers: Authorization: access token
    - Request example
      - ```
        GET https://staging.personicle.org/data/read/request?datatype=com.personicle.individual.datastreams.heartrate&startTime=2022-01-04%2015:54:12.092754&endTime=2022-04-04%2010:54:12.092918        
          ```

