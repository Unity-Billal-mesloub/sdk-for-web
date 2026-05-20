```javascript
import { Client, Storage, Compression, Permission, Role } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const storage = new Storage(client);

const result = await storage.updateBucket({
    bucketId: '<BUCKET_ID>',
    name: '<NAME>',
    permissions: [Permission.read(Role.any())], // optional
    fileSecurity: false, // optional
    enabled: false, // optional
    maximumFileSize: 1, // optional
    allowedFileExtensions: [], // optional
    compression: Compression.None, // optional
    encryption: false, // optional
    antivirus: false, // optional
    transformations: false // optional
});

console.log(result);
```