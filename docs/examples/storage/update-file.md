```javascript
import { Client, Storage, Permission, Role } from "appwrite";

const client = Client.from({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>' // Your project ID
});

const storage = new Storage(client);

const result = await storage.updateFile({
    bucketId: '<BUCKET_ID>',
    fileId: '<FILE_ID>',
    name: '<NAME>', // optional
    permissions: [Permission.read(Role.any())] // optional
});

console.log(result);
```