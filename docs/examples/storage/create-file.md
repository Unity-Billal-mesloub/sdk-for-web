```javascript
import { Client, Storage, Permission, Role } from "appwrite";

const client = Client.from({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>' // Your project ID
});

const storage = new Storage(client);

const result = await storage.createFile({
    bucketId: '<BUCKET_ID>',
    fileId: '<FILE_ID>',
    file: document.getElementById('uploader').files[0],
    permissions: [Permission.read(Role.any())] // optional
});

console.log(result);
```