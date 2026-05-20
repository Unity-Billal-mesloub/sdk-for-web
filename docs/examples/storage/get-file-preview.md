```javascript
import { Client, Storage, ImageGravity, ImageFormat } from "appwrite";

const client = Client.from({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>' // Your project ID
});

const storage = new Storage(client);

const result = storage.getFilePreview({
    bucketId: '<BUCKET_ID>',
    fileId: '<FILE_ID>',
    width: 0, // optional
    height: 0, // optional
    gravity: ImageGravity.Center, // optional
    quality: -1, // optional
    borderWidth: 0, // optional
    borderColor: '', // optional
    borderRadius: 0, // optional
    opacity: 0, // optional
    rotation: -360, // optional
    background: '', // optional
    output: ImageFormat.Jpg, // optional
    token: '<TOKEN>' // optional
});

console.log(result);
```