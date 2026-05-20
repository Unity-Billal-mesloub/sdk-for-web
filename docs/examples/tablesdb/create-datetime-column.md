```javascript
import { Client, TablesDB } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const tablesDB = new TablesDB(client);

const result = await tablesDB.createDatetimeColumn({
    databaseId: '<DATABASE_ID>',
    tableId: '<TABLE_ID>',
    key: '',
    required: false,
    xdefault: '2020-10-15T06:38:00.000+00:00', // optional
    array: false // optional
});

console.log(result);
```