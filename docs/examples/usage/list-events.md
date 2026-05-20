```javascript
import { Client, Usage } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const usage = new Usage(client);

const result = await usage.listEvents({
    queries: [], // optional
    total: false // optional
});

console.log(result);
```