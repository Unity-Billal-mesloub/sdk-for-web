```javascript
import { Client, Databases } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const databases = new Databases(client);

const result = await databases.createDocuments({
    databaseId: '<DATABASE_ID>',
    collectionId: '<COLLECTION_ID>',
    documents: [],
    transactionId: '<TRANSACTION_ID>' // optional
});

console.log(result);
```