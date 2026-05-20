```javascript
import { Client, Storage } from "appwrite";

const client = Client.from({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>' // Your project ID
});

const storage = new Storage(client);

const result = storage.getFileDownload({
    bucketId: '<BUCKET_ID>',
    fileId: '<FILE_ID>',
    token: '<TOKEN>' // optional
});

console.log(result);
```