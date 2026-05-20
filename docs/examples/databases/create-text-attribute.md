```javascript
import { Client, Databases } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const databases = new Databases(client);

const result = await databases.createTextAttribute({
    databaseId: '<DATABASE_ID>',
    collectionId: '<COLLECTION_ID>',
    key: '',
    required: false,
    xdefault: '<DEFAULT>', // optional
    array: false, // optional
    encrypt: false // optional
});

console.log(result);
```