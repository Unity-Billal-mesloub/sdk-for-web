```javascript
import { Client, Functions, ExecutionMethod } from "appwrite";

const client = Client.from({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>' // Your project ID
});

const functions = new Functions(client);

const result = await functions.createExecution({
    functionId: '<FUNCTION_ID>',
    body: '<BODY>', // optional
    async: false, // optional
    xpath: '<PATH>', // optional
    method: ExecutionMethod.GET, // optional
    headers: {}, // optional
    scheduledAt: '<SCHEDULED_AT>' // optional
});

console.log(result);
```