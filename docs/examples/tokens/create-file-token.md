```javascript
import { Client, Tokens } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const tokens = new Tokens(client);

const result = await tokens.createFileToken({
    bucketId: '<BUCKET_ID>',
    fileId: '<FILE_ID>',
    expire: '2020-10-15T06:38:00.000+00:00' // optional
});

console.log(result);
```