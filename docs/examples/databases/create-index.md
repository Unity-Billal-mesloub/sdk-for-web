```javascript
import { Client, Databases, DatabasesIndexType, OrderBy } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const databases = new Databases(client);

const result = await databases.createIndex({
    databaseId: '<DATABASE_ID>',
    collectionId: '<COLLECTION_ID>',
    key: '',
    type: DatabasesIndexType.Key,
    attributes: [],
    orders: [OrderBy.Asc], // optional
    lengths: [] // optional
});

console.log(result);
```