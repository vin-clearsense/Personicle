# Guidelines for contributing data connection to personicle
Open source developers can contribute connections to additional services for personicle. We have set up a template for data services and provide event hub producer modules for sending with the schema required for sending the data to personicle environment.

Three modules need to be implemented for adding an external service to personicle:

1. **OAuth2.0 workflow**: All wearable devices and data applications that provide data access via REST APIs use OAuth2.0 for securing user data. 
2. **Data download API calls**:
3. **Periodically triggered download**:

You can leverage the existing personicle infrastructure to run such applications. These modules can be implemented as functions in an Azure function app and utilize Azure storage queue for managing download requests.

You can find examples of such applications in the following 2 repositories:
1. Google fit download application [https://github.com/vaibhav-clearsense/data-download-apps]
2. Oura ring download application
