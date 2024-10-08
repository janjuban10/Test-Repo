Using Postman
Pre-request script to automatically get a new access token
When you send a request (i.e. GET, POST), Postman will check if the access_token variable exists. If not, it will run the Pre-request Script to get a new token
The new token will be stored in the environment variable access_token, and your request will automatically use it.
No need to manually request new tokens.
In Postman, the pm.sendRequest() function is asynchronous, meaning the rest of the script will execute before the sendRequest callback finishes. This is why the console might show null values because it's logging access_token before the token request is complete.
