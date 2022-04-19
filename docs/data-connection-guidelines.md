# Guidelines for contributing data connection to personicle
Open source developers can contribute connections to additional services for personicle. We have set up a template for data services and provide event hub producer modules for sending with the schema required for sending the data to personicle environment.

Three modules need to be implemented for adding an external service to personicle:

1. **OAuth2.0 workflow**: All wearable devices and data applications that provide data access via REST APIs use OAuth2.0 for securing user data. This needs to be implementged for every external service to obtain the required identity and access tokens.
2. **Data download API calls**: Once we have obtained an active access token for the user, we can start importing their data. Every data service has one or more data export API end points (there might be different end points for different data types), that provide access to user data. This module is specific to every service and would require the most development effort as API structure is different for every service. Once the data has been downloaded, the developer would need to map the data to a personicle data type (`utils/<service name>_data_mapping.py`). This mapping would be utilized while sending the data to personicle events edge.
3. **Periodically triggered download**: 

You can leverage the existing personicle infrastructure to run such applications. These modules can be implemented as functions in an Azure function app and utilize Azure storage queue for managing download requests.

In addition to the above 3 modules, the open source developers would also need access to the SQLAlchemy model for managing user credentials (e.g., access token for the service being integrated), schema for the data and events to be sent, and event hub producers to send the data to personicle environment. These are included in the azure function app as shared resources.

You can find examples of such applications in the following 2 repositories:
1. Google fit download application [https://github.com/vaibhav-clearsense/data-download-apps]
2. Oura ring download application [https://github.com/vaibhav-clearsense/oura-download-app]


