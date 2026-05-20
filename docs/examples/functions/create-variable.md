```javascript
import { Client, Functions } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const functions = new Functions(client);

const result = await functions.createVariable({
    functionId: '<FUNCTION_ID>',
    variableId: '<VARIABLE_ID>',
    key: '<KEY>',
    value: '<VALUE>',
    secret: false // optional
});

console.log(result);
```