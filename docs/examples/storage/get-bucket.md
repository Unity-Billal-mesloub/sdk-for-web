```javascript
import { Client, Storage } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const storage = new Storage(client);

const result = await storage.getBucket({
    bucketId: '<BUCKET_ID>'
});

console.log(result);
```