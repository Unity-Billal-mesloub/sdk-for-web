```javascript
import { Client, Functions } from "appwrite";

const client = Client.from({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>' // Your project ID
});

const functions = new Functions(client);

const result = await functions.listExecutions({
    functionId: '<FUNCTION_ID>',
    queries: [], // optional
    total: false // optional
});

console.log(result);
```