```javascript
import { Client, Sites } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const sites = new Sites(client);

const result = await sites.list({
    queries: [], // optional
    search: '<SEARCH>', // optional
    total: false // optional
});

console.log(result);
```