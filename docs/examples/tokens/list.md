```javascript
import { Client, Tokens } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const tokens = new Tokens(client);

const result = await tokens.list({
    bucketId: '<BUCKET_ID>',
    fileId: '<FILE_ID>',
    queries: [], // optional
    total: false // optional
});

console.log(result);
```