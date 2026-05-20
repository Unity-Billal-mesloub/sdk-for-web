```javascript
import { Client, Storage } from "appwrite";

const client = Client.from({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>' // Your project ID
});

const storage = new Storage(client);

const result = await storage.listFiles({
    bucketId: '<BUCKET_ID>',
    queries: [], // optional
    search: '<SEARCH>', // optional
    total: false // optional
});

console.log(result);
```