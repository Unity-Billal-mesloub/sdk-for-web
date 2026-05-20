```javascript
import { Client, TablesDB } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const tablesDB = new TablesDB(client);

const result = await tablesDB.deleteIndex({
    databaseId: '<DATABASE_ID>',
    tableId: '<TABLE_ID>',
    key: ''
});

console.log(result);
```